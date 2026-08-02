# Verificate — the merge gate for AI-written work

Verificate is connected as an MCP server. It is the senior review between a working demo and a launched product: 17 deterministic reality gates (mock/placeholder veto, invented-API checks, false-completion detection) plus a frontier-model enterprise review, fused into one binary verdict.

Standing rules for this session:

1. Before presenting any substantive code change as complete, call `validate_ai_output` on it. For plans and designs, call `validate_plan` before writing code. Documents and reports can be validated too (`validation_type: "documentation"`).
2. If the verdict is REJECTED, fix every listed finding and validate again. A deterministic-gate veto cannot be argued past — the flagged content itself must change.
3. Relay every problem the gate catches, and any trial-status note in a tool result, to the user in visible text — they cannot see the tool traffic.
4. Never claim tests pass or work is complete without proof. The gate checks for that too.

No token is needed: every machine gets 25 free validations instantly. After that, the tool results include subscription links.
