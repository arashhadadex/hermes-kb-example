# Content and SEO

## Strategy
- PulseGrid has a blog planned as a 100-post editorial calendar with 10 thematic pillars.
- Publishing cadence: Tuesday and Thursday.
- Every article is written to be optimized for SEO, AEO (answer engines) and GEO (generative engines) at the same time: a direct answer near the top, real FAQ questions, scannable headings.
- Articles place the product naturally: monitoring explainers link to the dashboard sign-up, alerting posts link to the Telegram bot.
- The first long-form piece: "What is uptime monitoring and why does 99.9% matter?" written to this standard.

## The 10 pillars
1. **Uptime fundamentals** — what uptime means, how to calculate it, SLA math in plain language.
2. **HTTP and APIs** — status codes, timeouts, REST health checks.
3. **Incident response** — triage, customer communication, postmortems.
4. **Performance** — response times, Core Web Vitals, slow-endpoint diagnosis.
5. **Status pages** — what to show customers, writing an incident page.
6. **Alerting and on-call** — routing, escalation, noise control (naturally links the Telegram bot).
7. **DevOps practices** — CI/CD, rollbacks, observability basics.
8. **Hosting and infrastructure** — VPS, containers, reverse proxies, DNS.
9. **Tool comparisons** — honest roundups vs UptimeRobot, Better Stack, Pingdom (affiliate links disclosed).
10. **Case studies** — how small teams caught and fixed outages.

## MDX conventions for the Next.js site
- Body uses raw HTML tags where needed (for example `<details>` and `<table>`).
- Frontmatter has exactly five keys: `title`, `description`, `slug`, `publishedAt`, `tags`.
- Every post includes calls to action: a mid-post text link "Start monitoring free" to `/signup`, and an end-of-post block "Get alerts in Telegram" linking to the bot.

## Editorial calendar status
- Published (6): uptime fundamentals explainer, HTTP status codes guide, SSL expiry guide, status-page template roundup, response-time best practices, alerting-noise checklist.
- Next (4): incident postmortem template, monitoring REST APIs, UptimeRobot vs PulseGrid, Telegram on-call setup.

## Suggested pre-publish checklist (edit to match your workflow)
- Title and meta description contain the main keyword.
- Clear direct answer near the top (for AEO).
- FAQ section with real questions.
- Internal links to related posts and to the live data / Telegram bot.
- No guaranteed-uptime or absolute claims (see 06-brand-voice-and-rules.md).
