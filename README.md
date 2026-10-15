# Hermes Agent knowledge-base example (PulseGrid)

A complete, ready-to-copy **business knowledge base** for a Telegram bot assistant built with Hermes Agent. This is the example folder used in the Hermes Agent + Telegram bot tutorial on [datatodeploy.com](https://datatodeploy.com).

**PulseGrid is a fictional uptime-monitoring service** invented for the tutorial. Every price, limit and command in these files is made up, the domains use the reserved `example.com` space and the bot handle is fake — nothing here points at a real product.

## What's in here

Nine markdown files, numbered in the order the agent should read them:

| File | Purpose |
|---|---|
| [00-README.md](00-README.md) | The entry point the agent reads first: file index and hard rules |
| [01-overview.md](01-overview.md) | What the product is, audience, positioning, business model |
| [02-product-features.md](02-product-features.md) | Features, limits and pricing |
| [03-telegram-bot.md](03-telegram-bot.md) | Bot commands, onboarding and alert message formats |
| [04-tech-and-infrastructure.md](04-tech-and-infrastructure.md) | Stack and architecture — no secrets, by rule |
| [05-content-and-seo.md](05-content-and-seo.md) | Blog strategy, calendar and MDX conventions |
| [06-brand-voice-and-rules.md](06-brand-voice-and-rules.md) | Tone of voice and hard rules (claims and disclaimers) |
| [07-roadmap-planned-features.md](07-roadmap-planned-features.md) | Ideas that are explicitly **not live** |
| [08-faq.md](08-faq.md) | Short answers the agent can reuse |
| [soul.md](soul.md) | Who the assistant is: identity, personality, boundaries |

`README.md` (this file) is for humans browsing the repository. `00-README.md` is the file actually given to the agent.

## How the setup works

1. Your Telegram bot forwards free-text messages to Hermes Agent.
2. Hermes Agent is pointed at this folder as its knowledge base.
3. The agent answers only from these files and admits when something is missing — it never invents prices, limits or features.

## Use it with your own business

1. Copy the folder.
2. Replace the PulseGrid facts and the fictional persona with your own — the example assistant is named "Pulse" in `soul.md`. Keep the file names and the four rules in `00-README.md` — they are what keep the agent from making things up:
   - answer only from these files;
   - roadmap items are never described as live;
   - no unmeasured or absolute claims;
   - if the owner contradicts a file in chat, trust the owner and suggest updating the file.
3. Anything you have not decided yet: leave it out of the files entirely instead of filling it with guesses. The rules above make the agent say "I don't know" instead.
4. Follow the tutorial on [datatodeploy.com](https://datatodeploy.com) to connect the folder to your Hermes Agent Telegram bot.

## Disclaimer

This repository is example material for a tutorial. PulseGrid, its prices, its statistics and its roadmap are all invented.
