---
type: decision
id: ADR-001
status: accepted
date: 2026-10-01
scope: vault
tags: [decision, meta, tooling, git]
---

# ADR-001 — How the vault stays in sync while building

Back to [[Home]] · Follows [[ADR-000 Note-taking tool]]

## Context
I want the vault to update **in parallel** while we build each module, not as one big import at the end. No Obsidian connector exists for Claude.

## Options considered
| Option | Pros | Cons |
|--------|------|------|
| Zip export per module | No setup | Manual imports; risk of overwriting my own edits |
| Link chat to my computer (Claude desktop app) | Zero setup; instant writes | Only works while the computer is on and the app is open |
| **Vault in a GitHub repo + Obsidian Git plugin** | Works even when my computer is off; full history of how notes evolved; phone can sync too | One-time setup (repo, plugin, auth) |

## Decision
**GitHub repo** `panchajanyabollam/system-design` is the vault. Claude commits notes; the **Obsidian Git** plugin auto-pulls them.

## Consequences
- ✅ Every decision gets committed when it's made, like real ADRs.
- ✅ `git log` shows how my understanding evolved.
- ⚠️ If I edit a note while Claude edits the same note, git may need a merge. Pull before editing.
- ⚠️ `.obsidian/workspace.json` is git-ignored to avoid constant conflicts.
