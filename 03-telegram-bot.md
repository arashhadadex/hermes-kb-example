# Telegram bot

## Role
The Telegram bot is PulseGrid's alert channel and support surface:
- It delivers incident alerts (down, recovered, SSL expiry).
- It answers free-text questions through Hermes Agent, which is given this folder as its knowledge base.
- Commands are handled natively by the bot service; only free-text messages are sent to the agent.

## Why Telegram only (decision)
PulseGrid focuses on Telegram and deliberately does not support Discord, because:
- Developers already keep Telegram open during incidents.
- Telegram's Bot API makes rich, fast alert messages straightforward.
- Supporting a second chat platform doubles onboarding and support work for little gain.

## Bot details
- Bot username: @pulsegrid_example_bot
- Commands:
  - `/start` — welcome message and a link to sign up
  - `/help` — list of commands with a one-line description each
  - `/connect CODE` — links the bot to your PulseGrid account (code valid 10 minutes)
  - `/monitors` — your monitors with id, name and current state
  - `/status` — one-line summary, e.g. "3 up, 1 down"
  - `/mute MINUTES` — silence all alerts for that long (max 1440)
  - `/feedback TEXT` — send a message to the team

## How a new user starts (onboarding)
1. Create an account at https://pulsegrid.example.com/signup
2. Dashboard → "Connect Telegram" → get a one-time 6-digit code
3. Open @pulsegrid_example_bot and send `/connect 123456`
4. The bot replies "Linked to alex@example.com — 3 monitors are watching." Alerts flow immediately for existing monitors.

## Example conversation (new monitor)
User adds `https://shop.example.org` in the dashboard, then receives:

> New monitor #42 — shop.example.org
> HTTP GET every 60 seconds from Frankfurt.
> Alerts: down, recovered. Change this in the dashboard.

## What happens when an alert triggers
> DOWN — shop.example.org
> HTTP 503 from Frankfurt after 2 failed checks.
> First failed 14:32 UTC, incident #8471 open.
> Reply /mute 60 to silence alerts for an hour, /monitors for the list.

When it closes:

> RECOVERED — shop.example.org is responding again (HTTP 200).
> Downtime: 7 minutes. Incident #8471 closed.

Repeat behaviour: one message when an incident opens, one when it closes. No repeats while an incident stays open. All timestamps are UTC.

## Common problems and fixes
- **Bot not replying:** you may have blocked it — unblock and send `/start`. The bot only replies in the private chat where you linked it.
- **Alerts not arriving:** the account link may have expired — re-link from the dashboard; or alerts are silenced — check with `/mute` or send `/status`.
- **Wrong monitor list:** make sure you linked the account you are signed in with (`/monitors` shows the linked email in its footer).
