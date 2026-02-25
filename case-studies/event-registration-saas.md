# Case Study: telegram-event-registration-service

## Context
Event organizers were losing registration requests in Telegram chats and had no reliable admin workflow for attendance operations.

## Goal
Build a production-ready service that keeps Telegram UX simple while giving organizers structured registration management.

## Solution
- Implemented monorepo architecture with bot runtime, admin UI, shared data layer, and SQL migrations.
- Added multi-tenant organization model with tenant-scoped admin API.
- Implemented lifecycle actions (`publish`, `close`, `promote`, `checkin`) and CSV export.

## Architecture Highlights
- `apps/bot`: Telegram webhook + admin API routes
- `apps/admin`: Next.js admin panel
- `packages/db`: typed data access against Supabase
- `supabase/migrations`: schema evolution and tenant isolation hardening

## Tech Stack
TypeScript, Node.js, Next.js, Telegraf, Supabase/PostgreSQL, Docker Compose.

## Outcome
- Reduced manual organizer operations with explicit admin endpoints.
- Added capacity/waitlist behavior and auditable export flow.
- Structured repository for CI and incremental feature delivery.

## Repository
- https://github.com/DenisArger/telegram-event-registration-service
