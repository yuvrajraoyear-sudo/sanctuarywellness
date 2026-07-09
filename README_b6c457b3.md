# Sanctuary Wellness by Play Haus — Documentation Index

Version 1.0 · draft for review

This is the master index for the Sanctuary specification. Eighteen documents in total: three foundational documents that define the brand and experience, and fifteen phase documents that carry the specification from product requirements to governance.

Read in the order below on a first pass. On revisit, each document is designed to stand on its own.

---

## Foundational documents

These describe *what Sanctuary is* before it becomes software.

| # | Document | What it defines |
|---|---|---|
| A | [doc-a-brand-bible.md](./doc-a-brand-bible.md) | Positioning, voice, visual identity, marks, guardrails |
| B | [doc-b-member-experience-blueprint.md](./doc-b-member-experience-blueprint.md) | The member journey from inquiry to loyalty, moment by moment |
| C | [doc-c-service-playbook.md](./doc-c-service-playbook.md) | On-the-floor service standards, ceremonies, and language |

---

## Phase documents

The build specification in fifteen ordered phases.

### Product & Experience

| # | Document | What it defines |
|---|---|---|
| 1 | [phase-1-prd.md](./phase-1-prd.md) | Product requirements, scope, success criteria |
| 2 | [phase-2-information-architecture.md](./phase-2-information-architecture.md) | Namespaces, routes, sitemap, super-app extensibility |
| 3 | [phase-3-database-schema.md](./phase-3-database-schema.md) | Postgres schema, relationships, RLS policies |
| 4 | [phase-4-user-flows.md](./phase-4-user-flows.md) | Ten primary flows as state machines, plus ancillary flows |
| 5 | [phase-5-design-system.md](./phase-5-design-system.md) | Tokens, components, motion vocabulary, a11y contract |

### Platform & Engineering

| # | Document | What it defines |
|---|---|---|
| 6 | [phase-6-api-spec.md](./phase-6-api-spec.md) | REST + realtime API surfaces, error codes, idempotency |
| 7 | [phase-7-nfr-architecture.md](./phase-7-nfr-architecture.md) | SLOs, perf budgets, regions, security, compliance, cost |
| 8 | [phase-8-ai-concierge.md](./phase-8-ai-concierge.md) | LLM strategy, safety, structured actions, evaluation |
| 9 | [phase-9-integrations.md](./phase-9-integrations.md) | Vendor map, adapter interfaces, exit plans |

### Business & Brand

| # | Document | What it defines |
|---|---|---|
| 10 | [phase-10-analytics-kpis.md](./phase-10-analytics-kpis.md) | North star (WRM), companions, guardrails, instrumentation |
| 11 | [phase-11-content-programming.md](./phase-11-content-programming.md) | Rituals, classes, events, editorial voice and calendar |
| 12 | [phase-12-operations.md](./phase-12-operations.md) | Org, daily rhythm, runbooks, staff enablement, SLAs |
| 13 | [phase-13-launch-gtm.md](./phase-13-launch-gtm.md) | Launch phasing, Founding Members, channels, pricing |

### Horizon & Governance

| # | Document | What it defines |
|---|---|---|
| 14 | [phase-14-post-launch-roadmap.md](./phase-14-post-launch-roadmap.md) | Year-1 quarterly plan, Year-2/3 themes, product bets |
| 15 | [phase-15-risks-governance.md](./phase-15-risks-governance.md) | Risk register, governance bodies, compliance, ethics |

---

## Reading paths

Depending on the reader, different orderings serve better.

- **Founder / investor:** A → B → 1 → 13 → 14 → 10 → 15
- **Product manager:** 1 → 2 → 4 → 5 → 6 → 8 → 10 → 11
- **Engineer:** 3 → 6 → 7 → 8 → 9 → 5 → 15
- **Designer:** A → B → 5 → 4 → 11 → C
- **Operator / GM:** B → C → 11 → 12 → 13 → 15
- **Legal / compliance:** 7 → 8 → 15 → 9 → 3

---

## Cross-cutting threads

Certain concepts appear across many documents. Track them here.

- **Weekly Restored Members (WRM)** — north-star metric. Defined in phase 10; guarded in 15; instrumented per 6, 3; surfaced in 12.
- **Concierge** — attributed AI whispers. Charter in 8; safety in 8, 12, 15; endpoints in 6; UX in 4, 5; whisper library in 11.
- **Recovery Index** — narrative band, never numeric. Defined in doc-b; computed by job in 6; whisper input in 8; not shared to LLM raw.
- **Ritual composition** — parent reservation + child slots. Schema in 3; flow in 4; endpoints in 6; content in 11.
- **Safety handoff** — LLM detects, server pages Ops, human responds. In 8, 12, 15; audited in 10.
- **DPDP / RBI / GST compliance** — in 7, 9, 15. Data-minimisation reflected in 6, 8.
- **Super-app namespacing** — `/sanctuary/`, `/sports/`, `/paradiso/`, `/kids/`. In 2; extended in 14 §7.

---

## Status

All 18 documents are v1.0 drafts for review. Each ends with a review checklist. Sign-off happens per document by the responsible council (see phase 15 §3).

Next steps after sign-off:
1. Assign owners for each open question in phase 4, 8, 15
2. Freeze v1.1 with resolutions
3. Break phase 1–7 into engineering tickets
4. Start P0 (internal) per phase 13 §2.1

---

## Document metadata

- Author: Sanctuary founding team
- Location context: Vasant Kunj, Delhi (V1)
- Regulatory context: India (DPDP Act 2023, GST, RBI e-mandate)
- Language: English (V1); Hindi content targeted Year-2
- Format: GitHub-flavoured Markdown, wrapped for readability

Comments, corrections, and pushbacks welcome. This is a working specification, not a monument.
