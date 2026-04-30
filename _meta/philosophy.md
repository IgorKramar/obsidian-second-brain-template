---
title: Vault Philosophy
type: meta
tags: []
---

# Vault Philosophy

Eleven principles behind the structure and rituals of this vault. Skim them before changing things — most weird design decisions become obvious once you know which principle they serve.

## 1. Minimum structure on start, grow when it hurts

No empty "future" folders. A folder appears the first time you genuinely don't know where to put a note. The vault is not a project — it should not become a place where you procrastinate from real work by reorganizing.

## 2. Linking > folders > tags

`[[wikilinks]]` are the primary connection mechanism. Folders are coarse buckets for very different kinds of content. Tags are facets (`#status/blocked`, `#domain/rust`), never a tree of topics.

## 3. Atomic + evergreen for knowledge

Notes about things you're learning live in `30-Resources/`. One thought = one note. Notes grow over time, get re-linked, and survive the project that birthed them. This is Zettelkasten (Luhmann / Ahrens / Matuschak).

## 4. Three levels of knowledge processing

- **Fleeting** — caught in `00-Inbox/`, processed within a few days
- **Literature** — notes summarizing external sources (book, article, video, podcast) with citations
- **Permanent / evergreen** — your own atomic claims, written for your future self

## 5. Frontmatter everywhere

Every note has YAML with `created`, `updated`, `type`, `tags`. This is the substrate Dataview queries on. `updated` is auto-maintained by the Update time on edit plugin.

## 6. MOCs (Maps of Content) instead of rigid folder hierarchies

For each topic that grows, create a `MOC-<topic>.md` with manual links to key notes plus a Dataview query that auto-collects everything tagged with that domain.

## 7. Templates per note type

Twenty templates in `_meta/templates/`. Templater applies them via folder triggers and creation events. Periodic Notes creates the file empty; Templater fills it on creation. Don't put a template in Periodic Notes' template field — that creates a race condition.

## 8. Reviews on decreasing cadence

Daily (5 min) → Weekly (15–20 min) → Monthly (30 min) → Quarterly (60 min). Calendar plugin shows what's been done; Tasks plugin tracks what's due.

## 9. AI context as a first-class document

`_ai-context/claude-starter.md` is the canonical onboarding doc for any new LLM session. It transcludes `personal-context`, `strategy`, current focus, current work week — so your model isn't asking you the same questions every time.

## 10. The daily note takes 5 minutes, not 25

If you find yourself avoiding the daily note, the template is too long. Cut fields ruthlessly. Energy/mood/gratitude is the floor. Everything else is optional.

## 11. Sync through your own private Git repo

No third-party paid sync. Clone the vault on each device, install Obsidian Git, let it auto-commit every 10 minutes. Conflicts are rare if you `git pull` before working.

## Anti-patterns to avoid

- Treating the vault as a project (decorating it instead of using it)
- Adding a folder "for later" before there's a single note that needs it
- Tagging by topic AND tagging by status — pick one fact per tag
- Keeping `personal-context.md` and `strategy.md` static for months — they should drift as you do
