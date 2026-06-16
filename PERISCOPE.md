# 🧿 Periscope: Give the Dragons Eyes

**The first major challenge and revenue wedge for Dragons Lair.**

### Goal
Transform language models into **active, tool-using agents** that perceive the real world, collaborate, and deliver verifiable utility — all scored under the Epistemic Hierarchy validator.

This proves decentralized dragons can outperform single centralized models on concrete tasks while remaining cartel-resistant.

### The Challenge

**Build Periscope** — a multi-agent system where dragons:
1. Receive a user query (e.g. longshoreman-style part lookup)
2. Plan, call tools, and collaborate
3. Submit full reasoning traces
4. Get scored by `DragonsLairValidator`

### Cartel Defense in Periscope

- **Liquid Patronage + Challenge Protocol**: Multiple agents can bid on the same task. Patrons stake on preferred agents. Any agent (or patron) can trigger a **stake-weighted contestation**. The validator re-audits the winning reasoning trace.
- **Reproducibility-First (60%)**: Collusion requires fabricating independent, logically sound reasoning chains at scale — exponentially expensive due to AST audit.
- **Utility Clawback (30%)**: If real-world outcome fails (wrong part, bad data), reputation and future rewards are clawed back publicly via the patron ledger.
- **Divergence Monitoring**: Shadow diagnostics flag suspicious consensus patterns.

Result: Collusion is more expensive than honest specialization.

### Tool Interface (MVP)

Agents use **structured function calling** (compatible with Claude/Grok-style tool_use or OpenAI format). Initial tools:
- `web_search(query)`
- `scrape_url(url, instructions)`
- `visual_search(image_description or url)`
- `cross_reference(data_sources)`

Future: Custom AST-based dispatch layer for full traceability.

### Epistemic Hierarchy Integration

Every agent submission includes a reasoning trace. The validator runs:
```python
audit_score = verify_reproducibility_audit(logic_path)  # 60%
utility_score = confirm_utility(real_outcome)           # 30%
consensus_score = get_network_consensus(...)            # 10%
```

### Example Task (Domain-Grounded)

"A passenger on Europa 2 needs a replacement bearing for a specific mooring winch. Find exact OEM part number, current supplier pricing in LA port area, and 48-hour availability."

### Phase 1 (Immediate – Local Simulation)

- Mock tool harness (pre-built responses + logging)
- Single and multi-agent test scenarios
- Full validator scoring pipeline
- Patron ledger + dashboard UI stub

What a co-founder would build first: Real tool connectors + improved AST auditor.

### Why Periscope Wins

- **Proof**: Dragons solve problems they weren't explicitly trained for.
- **Revenue**: First vertical for paying customers (logistics, research, parts matching).
- **Stress Test**: Real data exposes weaknesses in the Epistemic Hierarchy fast.

### Next Steps After Periscope PoC

- Live web tools
- Multi-agent debate + resolution
- Bittensor testnet deployment
- First customer pilots
