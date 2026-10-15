# Tech and infrastructure

> Never put passwords, API keys, tokens, IP addresses or ports in this file. Its contents are sent to the AI model provider.

## Stack
- Frontend: Next.js 15 (App Router), TypeScript, MDX for the blog.
- Backend: Python 3.12, FastAPI, SQLAlchemy, Alembic.
- Telegram bot: separate Python service using aiogram 3, calling the backend over HTTP.
- Checks: worker processes consuming a Redis queue; HTTP requests made with httpx; SSL expiry read from the certificate during the check.
- Databases: PostgreSQL 16 (users, monitors, incidents, check results — retained per plan: 30 days / 90 days / 1 year by a nightly pruning job) and Redis 7 (check queue, rate limiting).

## Hosting
- One Linux VPS, Docker Compose, Caddy as the reverse proxy (automatic HTTPS).
- DNS managed in Cloudflare; the website sits behind Cloudflare's CDN, while the bot and API talk to Telegram directly from the VPS.
- GitHub Actions runs tests on every push; deploy is a script on the VPS that pulls, rebuilds the changed service and restarts it.

## Architecture
- Scheduling: each monitor has a `next_check_at` timestamp; workers pop due checks from Redis, run the HTTP request with a 10-second timeout and write the result.
- Alerting: after 2 consecutive failures an incident opens and the bot service is called; the first success closes it. The bot service sends the message via the Telegram Bot API and enforces exactly one message per incident edge (start and end).
- Repos and layout: pulsegrid-web (frontend), pulsegrid-api (backend), pulsegrid-bot (bot service), infra (Compose files, Caddy config, deploy script).
- Known issues / tech debt: checks run from a single region (Frankfurt) so a local outage looks global; result pruning is an unmonitored cron job; the bot retries a failed Telegram send only once.
