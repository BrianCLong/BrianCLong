# Brian Long

**Founder & CEO, [Summit Cognitive](https://summitcognitive.ai)**

Summit Cognitive builds the runtime admissibility layer for AI in high-stakes decisions. Its product, the **Decision Receipt**, turns a machine-made decision into a cryptographically signed, replayable, independently verifiable record of why an output was allowed, revised, blocked, or escalated.

---

### The problem

Autonomous systems are being handed decisions that carry consequence — merges, deployments, filings, denials, escalations. When one of those decisions is later challenged, most stacks can produce a log. Very few can produce an account: what evidence was in hand, which policy applied, whether the same inputs would reach the same conclusion again, and who held the right to decide.

Regulators are converging on the same expectation. The EU AI Act's record-keeping and traceability duties — Articles 12, 19 and 26(6) — are architectural obligations, not retention-shelf items. Retrofitting an evidence layer under an already-running agent network is materially harder than instrumenting one still being built.

### What I build

- **Decision Receipt** — every governed action ships a receipt: Ed25519-signed, hash-chained to its predecessor so the record is tamper-evident, and verifiable offline against a published public key.
- **Admissibility gate** — evidence in, policy evaluated, verdict out: `ALLOWED` · `BLOCKED` · `ESCALATED`, with a replay determination recording whether the decision reproduces deterministically.
- **IntelGraph** — graph intelligence linking decisions to the evidence, entities and relationships behind them.
- **Maestro** — orchestration for multi-agent workflows under explicit governance and observability.
- **Temporal** — bitemporal audit, so you can ask not just what was true, but what was known when.

### Try it

The service is live and the read endpoints need no key.

```bash
# Service health
curl -s https://decrec.summitcognitive.ai/health

# The Ed25519 public key receipts are verified against
curl -s https://decrec.summitcognitive.ai/v1/keys/server

# Free-tier API key (100 req/hr)
curl -s https://decrec.summitcognitive.ai/v1/signup \
  -H 'Content-Type: application/json' \
  -d '{"email":"you@example.com"}' | jq -r .api_key
```

Full recipes: [docs.summitcognitive.ai/guides/examples](https://docs.summitcognitive.ai/guides/examples)

### Where things live

| | |
| --- | --- |
| Company | [summitcognitive.ai](https://summitcognitive.ai) |
| Developer docs | [docs.summitcognitive.ai](https://docs.summitcognitive.ai) |
| Live service | [decrec.summitcognitive.ai](https://decrec.summitcognitive.ai) |
| Demos | [demo.summitcognitive.ai](https://demo.summitcognitive.ai) |
| Trust portal | [trust.summitcognitive.ai](https://trust.summitcognitive.ai) |
| Press & media | [press.summitcognitive.ai](https://press.summitcognitive.ai) |
| Engineering org | [@Summit-Cognitive](https://github.com/Summit-Cognitive) |

### The claim I don't overstate

A receipt that verifies is proof **about the record** — that the inputs, the policy and the outcome are what they claim to be, unaltered and in order. It is not a warranty that the model was right. Correctness stays a human judgement. What the receipt changes is that the judgement becomes reviewable instead of unreviewable.

### Background

Two decades of cyber, media and intelligence work on institutional decision systems and cognitive infrastructure. Summit Cognitive is a Delaware C-corporation founded April 2026, headquartered in Alma, Colorado.

### Work with me

Enterprise pilots, regulated deployments, and cognitive security engagements — including the 30-day Decision Admissibility Pilot.

**brian@summitcognitive.ai** · [LinkedIn](https://www.linkedin.com/in/bcl23) · [ORCID 0009-0001-2058-5769](https://orcid.org/0009-0001-2058-5769)
