# PulseGrid — overview

## What it is
PulseGrid is a website uptime-monitoring web app with an associated Telegram bot. Users add URLs to watch on the site and receive alerts in Telegram when something goes down.

## Who builds it
Alex Morgan, an independent full-stack developer. (Fictional persona for this example.) He handles the code, infrastructure and content himself.

## Audience
Small SaaS teams, indie developers and agencies running a handful of production sites who want fast outage alerts without building their own monitoring stack. Primary markets: Europe and North America. Product and docs are English-only.

## Value proposition
Setup takes about two minutes: paste a URL, connect Telegram, done. No agents to install and no config files to write, and the free tier covers a side project's full footprint. Alerts arrive in Telegram, where on-call developers already are, instead of in another dashboard nobody opens.

## Competitors / alternatives
- **UptimeRobot** — generous free tier, but alert routing is email-first and Telegram linking takes several clicks.
- **Better Stack** — polished incident timelines, but priced per monitor and aimed at larger teams.
- **Pingdom** — mature brand with deep checks, but expensive at the monitor counts a solo developer needs.

PulseGrid competes on Telegram-first alerts, setup speed and flat workspace pricing.

## Business model
Free tier plus two paid plans (Free / Pro / Business — details in 02-product-features.md). Blog tool roundups may include affiliate links; they are always disclosed (see 06-brand-voice-and-rules.md). No ads.

## Current stage
Public beta since March 2026. About 250 users watching roughly 3,000 endpoints. Growth comes mostly from the blog and the Telegram channel.

## Key links
- Website: https://pulsegrid.example.com
- Telegram bot: @pulsegrid_example_bot
- GitHub: github.com/pulsegrid-demo (repos: pulsegrid-web, pulsegrid-api, pulsegrid-bot, infra)
- Status page: https://status.pulsegrid.example.com
