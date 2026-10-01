---
type: concept
tags: [concept, process]
created: 2026-10-01
---

# Architecture Decision Record (ADR)

A short document capturing **one** important technical decision: why it was made, what else was considered, and what it costs. Real engineering teams keep these so that, months later, nobody has to guess *why* the system looks the way it does.

## The four sections
1. **Context** — the problem and the forces at play
2. **Options considered** — each alternative with pros and cons
3. **Decision** — what was chosen
4. **Consequences** — trade-offs accepted, follow-up work

## Rules of thumb
- One decision per ADR; number them (`ADR-001`, `ADR-002` …).
- Never edit an accepted ADR's decision. If it changes, write a new ADR that **supersedes** it.
- Write it *when* the decision is made, not afterwards.

## Used in
- [[ADR-000 Note-taking tool]]
- [[ADR-001 Vault sync method]]
- Template: [[Templates/ADR Template|ADR Template]]
