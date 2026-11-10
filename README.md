# Verificate for Gemini CLI / Antigravity

[![Verificate Gate](https://img.shields.io/badge/gated%20by-Verificate%20Gate-2ea44f?logo=shield&logoColor=white)](https://github.com/VerificateAI/verificate-gate-action)


**Your vibe-coded MVP, all the way to production.** Between a working demo and a launched product used to stand an experienced CTO and a senior dev team — the people who catch the mock refund path, the invented SDK call, the loop that dies at real traffic. This extension puts that review inside Gemini CLI, with power to **veto**.

## Install

```bash
gemini extensions install https://github.com/VerificateAI/verificate-gemini-extension
```

That's it. **100 free validations per machine — no account, no card, no token.** The extension connects to the hosted Verificate MCP server (`https://mcp.verificate.ai/mcp`) and adds a standing rule so Gemini validates substantive changes before presenting them as done.

### Antigravity

Antigravity CLI imports this extension (`agy plugin import gemini`). To add the server natively instead, put this in Antigravity's `mcp_config.json`:

```json
{
  "mcpServers": {
    "verificate": { "serverUrl": "https://mcp.verificate.ai/mcp" }
  }
}
```

## What you get

| Tool | Job |
|---|---|
| `validate_ai_output` | The merge gate for AI-written code **and documents** — deterministic veto checks (mocks and placeholders, reward-gamed tests, invented standard-library APIs, secrets in logs, false-completion claims) (any one can veto), then a Claude Haiku 5.5 review (ISO/IEC 25010, ISO/IEC 5055). One decision with severity-ranked findings and a receipt. |
| `validate_plan` | The same gate for plans and designs, before any code exists. |
| `analyze_code` | Advisory deep-dive — performance hot paths, scalability cliffs, failure modes. No verdict, never blocks. |
| `generate_code` | Generate + gate in one step. |

A real rejection, verbatim from the production gateway: *"N+1 synchronous API calls … will trigger Stripe rate limiting (100 req/sec limit)"* · *"`stripe.Inventory` is not a valid Stripe SDK resource"* · *"Stripe API requires integer cents."* Each of those is an afternoon of production debugging, caught in seconds.

## Keep going after the free 100

Sign up at <https://verificate.ai/auth/signup> (30-day trial, no card — then $30/mo) and add your token to the extension's server config:

```json
"mcpServers": {
  "verificate": {
    "httpUrl": "https://mcp.verificate.ai/mcp",
    "headers": { "Authorization": "Bearer YOUR_TOKEN" }
  }
}
```

## Privacy

Code you validate is analyzed, never executed, and never used to train models. Privacy policy: <https://verificate.ai/privacy> · Terms: <https://verificate.ai/terms>

---

Main repo (all clients, one-click installs): [VerificateAI/verificate-mcp-quickstart](https://github.com/VerificateAI/verificate-mcp-quickstart) · Website: <https://verificate.ai/mcp>
