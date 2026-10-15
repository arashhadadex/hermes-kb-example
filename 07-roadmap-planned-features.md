# Roadmap — planned or under evaluation (NONE OF THIS IS LIVE)

These are ideas Alex has evaluated for PulseGrid. Do not tell users they exist.

1. **Multi-region checkers:** run each check from Frankfurt, New York and Singapore, and open an incident only when 2 of 3 regions fail. Ship criteria: the queue carries 10× current volume and per-region results show in the dashboard.
2. **Natural-language alert rules:** type "tell me if shop.example.org is slower than 800ms during checkout" and the system parses it into a rule. Ship criteria: parsed rules round-trip through a review screen before saving, and the false-rule rate stays under 5% in internal testing.
3. **Incident summaries with LLM explanations:** each closed incident gets a plain-language summary (what failed, since when, what recovered). Ship criteria: summaries never block or delay alert delivery.
4. **Hermes Agent actions in the bot:** pause, resume and add monitors from chat behind an explicit confirmation step. Ship criteria: confirmation flow, an audit log of every chat-initiated action, and a rollback-friendly design — all three before any chat action ships.
5. **MCP server exposing PulseGrid data and actions to AI tools.** Ship criteria: read-only first (list monitors, latest incidents); per-action token scopes only after item 4 is live.

## Priorities (in order)
1. Multi-region checkers — blocked until the volume test above passes.
2. Hermes Agent actions in the bot — blocked on the confirmation flow and audit log.
3. Incident summaries — after multi-region, since summaries depend on per-region data.
4. Natural-language rules — after actions, because both reuse the same review screen.
5. MCP server — last; read-only endpoints wait for stable API versioning.
