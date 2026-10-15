# FAQ (short answers the agent can reuse)

**What is PulseGrid?**
A website uptime-monitoring web app with a Telegram bot for alerts.

**How much does it cost?**
Free for 5 monitors. Pro is $9/month (50 monitors), Business is $29/month (250 monitors) — per workspace, billed monthly, 14-day trial on paid plans with no card required.

**Which checks are supported?**
HTTP(S) GET or HEAD on every plan. Pro and Business add response-time thresholds, keyword presence and TCP port checks. Checks run every 60 seconds on Free and every 15 seconds on paid plans.

**How do I set up a Telegram alert?**
Sign up, add a monitor in the dashboard, then Dashboard → Connect Telegram → send the one-time code as `/connect 123456` to @pulsegrid_example_bot. Alerts for your monitors start immediately.

**Can I get alerts on Discord?**
No. Telegram only, by design.

**Does PulseGrid prevent outages?**
No. It detects them and notifies you by Telegram and email; fixing the outage is up to you.

**Can PulseGrid fix an outage for me?**
No. It cannot restart your services or change your DNS.

**Is there a public API or MCP server?**
Not yet. An MCP server is being evaluated but is not live — see 07-roadmap-planned-features.md.

**How do I contact support?**
support@pulsegrid.example.com or `/feedback` in the bot — replies within 2 business days.
