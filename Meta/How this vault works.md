---
type: meta
tags: [meta]
created: 2026-10-01
---

# How this vault works

Back to [[Home]]

## Folder layout
```
Home.md                 ← start here
Roadmap.md              ← all tracks & modules
Concepts/               ← reusable ideas, linked from many modules (graph hubs)
Modules/
  01 - TinyURL/
    TinyURL.md          ← module overview / Map of Content
    Estimations.md      ← QPS, storage, bandwidth, cache size
    Tech Stack.md       ← what was used and why
    Decisions/          ← one ADR per decision
    Build Log.md        ← components in build order
    Lessons.md          ← what broke, what I'd change
Meta/                   ← decisions about the vault itself
Resources/              ← books & articles
Templates/              ← ADR and module templates
```

## Note types (`type:` in frontmatter)
| type | What it is |
|------|------------|
| `moc` | Index page ([[Map of Content]]) |
| `module` | A module overview |
| `concept` | A reusable system design idea |
| `decision` | An [[Architecture Decision Record]] |
| `estimation` | [[Back-of-the-envelope Estimation]] |
| `resource` | Book or article |
| `meta` | About the vault itself |

## Graph view tips
In Graph view → **Groups**, add color groups:
- `path:Concepts` → blue
- `path:Decisions OR path:Meta` → orange
- `path:Modules` → green
- `path:Resources` → purple

Turn on **Existing files only** to hide ghost nodes, or leave it off to see concepts that are linked but not written yet.

## Sync
Claude commits notes to the GitHub repo while we build; Obsidian Git pulls them in. See [[ADR-001 Vault sync method]].
