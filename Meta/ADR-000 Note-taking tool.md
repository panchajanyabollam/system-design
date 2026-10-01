---
type: decision
id: ADR-000
status: accepted
date: 2026-10-01
scope: vault
tags: [decision, meta, tooling]
---

# ADR-000 — Note-taking tool for the learning vault

Back to [[Home]] · Format: [[Architecture Decision Record]]

## Context
After each module I want to revisit everything: calculations, decisions, tech stack, alternatives. I need a place that is fast to browse, links ideas across modules, and lasts for years.

## Options considered
| Option | Pros | Cons |
|--------|------|------|
| **Obsidian** | Plain Markdown on disk; very fast; `[[links]]` + graph view; Dataview for querying decisions; git-friendly; Mermaid built in | Plugins needed for some features; sync needs setup |
| **Notion** | Polished databases and toggles; easy sharing; already connected to Claude | Slower; cloud-dependent; content locked in Notion |
| Plain `docs/` in each repo | Notes live next to code | No graph, no cross-module linking |

## Decision
**Obsidian**, with the vault stored in a git repo.

## Consequences
- ✅ Concepts become hubs that link modules together in the graph.
- ✅ Notes are portable Markdown and versioned in git.
- ⚠️ Need a sync method → see [[ADR-001 Vault sync method]].
