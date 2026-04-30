# Obsidian Second Brain Template

A personal "second brain" Obsidian vault template — folder structure, frontmatter conventions, 20 ready Templater templates, weekly/monthly review rituals, and an AI-context starter pack for feeding stable context into LLM sessions.

> Built and used by [@IgorKramar](https://github.com/IgorKramar). Public template; the live private vault is separate. Improvements occasionally backported here by hand.

## Why this exists

Most "second brain" advice is either too philosophical (Zettelkasten purity) or too narrow (one specific app's tutorial). This template is opinionated middle ground: enough structure that you start using it on day one, light enough that you don't drown in meta-work.

## What's inside

```
.
├── 00-Inbox/                # fleeting notes, ideas, quick captures
├── 01-Daily/                # daily / weekly / monthly notes (Periodic Notes)
├── 10-Areas/                # ongoing life domains (work, health, family, finance, …)
├── 20-Projects/             # things with a deadline or done-state
├── 30-Resources/            # Zettelkasten zone — atomic notes + topical MOCs
├── 40-People/               # CRM-style notes on people
├── 50-Reference/            # cheatsheets, snippets, recipes
├── 90-Archive/              # closed and put away
├── _ai-context/             # starter packs for Claude/LLM sessions
└── _meta/
    ├── conventions.md       # frontmatter, naming, tag rules
    ├── rituals.md           # daily/weekly/monthly/quarterly review cadence
    ├── philosophy.md        # 11 principles behind the structure
    └── templates/           # 20 Templater templates
```

## Get started

1. Clone:
   ```bash
   git clone https://github.com/IgorKramar/obsidian-second-brain-template.git my-vault
   cd my-vault
   ```
2. Open as a vault in Obsidian (`File → Open vault → Open folder as vault`).
3. Trust the author and enable community plugins (Obsidian will prompt).
4. Install the recommended plugins from `community-plugins.json`. Each one's `data.json` is already pre-configured.

   Recommended plugins (install through Settings → Community plugins → Browse):

   - Templater
   - Periodic Notes
   - Dataview
   - Update time on edit
   - Folder notes
   - Tasks
   - Calendar
   - Tag Wrangler
   - Advanced Tables
   - Linter
   - Obsidian Git
   - QuickAdd
   - Omnisearch (optional, replaces built-in search)

5. Set Folder Notes "Storage location" to **In the parent folder**.
6. Periodic Notes — enable Daily/Weekly/Monthly, point each at `_meta/templates/{daily,weekly,monthly}.md` (or leave the template field empty and let Templater handle it via folder templates — see `_meta/philosophy.md`).
7. Fill in your own `10-Areas/personal-context.md`, `strategy.md`, and `family.md`. The scaffolds are intentionally empty.
8. Optional: install a theme you like (the original author uses Obsidian gruvbox).

## How to use

- **Daily** (5–7 min, evening) — fill the daily note, drop into `health/metrics/<date>.md` whatever metrics you care about
- **Weekly work** (Friday, 15–20 min) — review the week, refresh `_ai-context/work-current-week.md`
- **Weekly health** (Sunday, 10 min) — review metrics, refresh `_ai-context/current-focus.md` for the next week
- **Monthly** (last day of month, 30 min) — monthly note + finance summary in `10-Areas/finance/monthly/`
- **Quarterly** (e.g. Aug 1, Nov 1) — re-read `strategy.md`, decide what holds and what changes

The full review schedule lives in `_meta/rituals.md` as recurring Tasks-plugin entries.

## AI context starter pack

`_ai-context/claude-starter.md` is a wrapper that uses Obsidian transclusion (`![[file]]`) to embed your `personal-context`, `strategy`, current focus, and current work week into one document. Open it in Read view, copy the rendered output, paste into a new Claude/LLM session — the model now knows who you are.

## Philosophy

See `_meta/philosophy.md`. Short version:

- Linking > folders > tags
- Minimum structure on start, grow when it hurts
- Atomic + evergreen for knowledge (Zettelkasten in `30-Resources/`)
- Frontmatter everywhere — for Dataview queries
- Daily note takes 5 minutes, not 25
- Sync via your own private Git repo

## License

MIT — do whatever you want, no warranty. See `LICENSE`.
