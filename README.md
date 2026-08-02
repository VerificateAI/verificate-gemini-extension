# Verificate for Gemini CLI / Antigravity

**Your vibe-coded MVP, all the way to production.** Between a working demo and a launched product used to stand an experienced CTO and a senior dev team — the people who catch the mock refund path, the invented SDK call, the loop that dies at real traffic. This extension puts that review inside Gemini CLI, with power to **veto**.

## Install

```bash
gemini extensions install https://github.com/Verificate-Dev/verificate-gemini-extension
```

That's it. **25 free validations per machine — no account, no card, no token.** The extension connects to the hosted Verificate MCP server (`https://mcp.verificate.ai/mcp`) and adds a standing rule so Gemini validates substantive changes before presenting them as done.

## What you get

| Tool | Job |
|---|---|
| `validate_ai_output` | The merge gate for AI-written code **and documents** — 17 deterministic reality gates (any one can veto), then a frontier-model enterprise review. Binary approve/reject with severity-ranked findings. |
| `validate_plan` | The same gate for plans and designs, before any code exists. |
| `analyze_code` | Advisory deep-dive — performance hot paths, scalability cliffs, failure modes. No verdict, never blocks. |
| `generate_code` | Generate + gate in one step. |

A real rejection, verbatim from the production gateway: *"N+1 synchronous API calls … will trigger Stripe rate limiting (100 req/sec limit)"* · *"`stripe.Inventory` is not a valid Stripe SDK resource"* · *"Stripe API requires integer cents."* Each of those is an afternoon of production debugging, caught in seconds.

## Keep going after the free 25

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

Main repo (all clients, one-click installs): [Verificate-Dev/verificate-mcp-quickstart](https://github.com/Verificate-Dev/verificate-mcp-quickstart) · Website: <https://verificate.ai/mcp>
