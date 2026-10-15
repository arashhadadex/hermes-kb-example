# Product features

## Confirmed (live today)
- HTTP(S) uptime checks (GET or HEAD) with a 10-second timeout.
- Check interval: 60 seconds on Free, 15 seconds on Pro and Business.
- An incident opens after 2 consecutive failed checks and closes on the first successful check.
- Alerts delivered through the Telegram bot and by email.
- Alert types: monitor down, monitor recovered, SSL certificate expiring in 14 days or less.
- Pro adds: response-time threshold alerts, keyword presence checks, TCP port checks.
- Dashboard: monitor list, 30-day uptime bars, incident history, response-time chart.
- Accounts: sign up with email on the website. Telegram is linked with a one-time code (see 03-telegram-bot.md).

## Limits and pricing
| | Free | Pro — $9/month | Business — $29/month |
|---|---|---|---|
| Monitors | 5 | 50 | 250 |
| Check interval | 60s | 15s | 15s |
| History | 30 days | 90 days | 1 year |
| Team members | 1 | 3 | 5 |
| Status pages | — | 1 | 10 |
| Keyword / TCP / response-time checks | — | yes | yes |

Prices are per workspace, billed monthly, cancel any time. Pro and Business start with a 14-day trial; no card required.

## Not available
- Discord notifications (Telegram only, on purpose — see 03-telegram-bot.md).
- SMS and phone calls.
- Agents installed on your server (checks are external HTTP requests only).
- Anything listed in 07-roadmap-planned-features.md.
