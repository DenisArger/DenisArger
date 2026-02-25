# Case Study: work-reports

## Context
Managers needed periodic summaries from Google Drive/Sheets reports, but manual collection was time-consuming and inconsistent.

## Goal
Automate report aggregation in Telegram with minimal operator effort and clear admin-only controls.

## Solution
- Built Telegram webhook handlers as serverless functions.
- Integrated Google APIs for file discovery and summary generation.
- Added command workflows (`/reports`, `/today`, support/help commands) with admin checks and dedup logic.

## Architecture Highlights
- `api/telegram.ts`: command parsing, routing, and response logic
- `lib/googleDrive`: report collection and document generation
- `lib/telegram`: delivery layer for bot replies
- Vercel deployment with env-driven configuration

## Tech Stack
TypeScript, Node.js, Google APIs, Vercel, Telegram Bot API.

## Outcome
- Converted repetitive manual reporting into command-driven automation.
- Improved consistency of reporting output and operator response time.
- Repository hardened with docs, CI, and license.

## Repository
- https://github.com/DenisArger/work-reports
