<div align="center">

# Obsidian Second Brain

**English** · [Русский](README.ru.md)

### Capture. Connect. Review.

20 note templates · periodic reviews · a portable Markdown vault

[![MIT](https://img.shields.io/badge/license-MIT-9ece6a?style=flat-square)](LICENSE)
![Obsidian](https://img.shields.io/badge/Obsidian-7C3AED?style=flat-square&logo=obsidian&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-000000?style=flat-square&logo=markdown&logoColor=white)
![Templater](https://img.shields.io/badge/templates-Templater-7aa2f7?style=flat-square)

[Start](#get-started) · [Layout](#vault-layout) · [Rituals](#daily-use) · [Context](#context-starter-pack) · [Guides](#guides)

</div>

A personal knowledge vault with enough structure to use on day one: frontmatter conventions, reusable notes, project and life areas, and weekly/monthly reviews. Linking comes first; folders provide broad buckets and tags add facets.

This is a **public template**, separate from the author's private vault. Improvements are occasionally backported manually. The entry documentation is available in English and Russian; included notes and templates use both languages.

## Get started

1. Clone the template:

   ```sh
   git clone https://github.com/IgorKramar/obsidian-second-brain-template.git my-vault
   cd my-vault
   git remote remove origin
   ```

   Removing the template remote keeps a future push from targeting this public repository. If you want Git sync, add **your own private repository** before recording personal information.

2. Open `my-vault` in Obsidian with **Open folder as vault**.
3. Review the included configuration, then enable community plugins if you trust it. Install plugins through **Settings → Community plugins → Browse**; plugin code is not bundled.
4. Use the recommended plugin list below. Settings are included for most plugins in [.obsidian/plugins/](.obsidian/plugins/).
5. Set Folder Notes storage to **In the parent folder**. Periodic Notes has Daily/Weekly/Monthly folders configured; leave its template fields empty to use the included Templater folder mappings. Avoid applying the same template twice.
6. Fill in [personal context](10-Areas/personal-context.md), [strategy](10-Areas/strategy.md) and [family](10-Areas/family.md); these are deliberately blank scaffolds.
7. Choose any theme you like; no theme files are included. The author's original preference is Obsidian gruvbox.

<details>
<summary><strong>Recommended community plugins</strong></summary>

The exact IDs are in [community-plugins.json](.obsidian/community-plugins.json).

| Purpose | Plugins |
|:---|:---|
| Notes and dates | Templater, Periodic Notes, Calendar, Folder notes |
| Queries and tasks | Dataview, Tasks |
| Editing | Update time on edit, Advanced Tables, Linter, Tag Wrangler |
| Capture and search | QuickAdd, Omnisearch (optional alternative to built-in search) |
| Version history | Obsidian Git |

Obsidian Git's included configuration enables automatic commits every 10 minutes and pull on startup. Automatic push has an interval of zero, but manual push is enabled. Review the settings and repository destination before using it with personal notes.

</details>

## Vault layout

| Path | What goes here |
|:---|:---|
| [00-Inbox/](00-Inbox/) | Fleeting notes and quick captures |
| [01-Daily/](01-Daily/) | Daily, weekly and monthly notes |
| [10-Areas/](10-Areas/) | Ongoing work, health, family and finance |
| [20-Projects/](20-Projects/) | Work with a deadline or a done-state |
| [30-Resources/](30-Resources/) | Atomic knowledge notes and maps of content |
| [40-People/](40-People/) | Notes about people |
| [50-Reference/](50-Reference/) | Cheatsheets, recipes and snippets |
| [90-Archive/](90-Archive/) | Completed or inactive material |
| [_ai-context/](_ai-context/) | Context packs for language-model sessions |
| [_meta/](_meta/) | Conventions, rituals and 20 Templater templates |

Use wikilinks to connect ideas. Add frontmatter for Dataview queries. Keep knowledge notes atomic and useful beyond a single project; grow the structure only when your notes need it.

## Daily use

| Rhythm | Suggested practice |
|:---|:---|
| Daily · 5–7 minutes | Fill in the daily note; optionally record health metrics in `10-Areas/health/metrics/` |
| Friday · 15–20 minutes | Review the work week and update `_ai-context/work-current-week.md` |
| Sunday · 10 minutes | Review health and update `_ai-context/current-focus.md` |
| Month end · 30 minutes | Monthly review and finance summary in `10-Areas/finance/monthly/` |
| Quarterly | Revisit `10-Areas/strategy.md` and adjust your direction |

The [ritual guide](_meta/rituals.md) includes the detailed schedule and recurring Tasks entries. The cadence is a starting point; adapt it to your life.

## Context starter pack

The [starter document](_ai-context/claude-starter.md) uses Obsidian transclusion (`![[file]]`) to assemble personal context, strategy, current focus and the work week. Open it in Reading view and copy the rendered text into a new language-model session when useful.

Review the rendered content before sharing it: the finished vault can contain private family, health, finance or work information. Sharing a context pack is an explicit action, not part of vault synchronization.

## Guides

| Document | Language | Covers |
|:---|:---|:---|
| [Conventions](_meta/conventions.md) | Russian | Frontmatter, note types, naming and tags |
| [Philosophy](_meta/philosophy.md) | English | Eleven principles behind the layout |
| [Rituals](_meta/rituals.md) | Russian | Review steps and recurring tasks |
| [Templates](_meta/templates/) | Mixed EN/RU | Daily notes, projects, people, books, decisions and more |

## License

[MIT](LICENSE) · Igor Kramar. Third-party Obsidian plugins retain their own licenses.
