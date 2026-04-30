---
title: Vault Conventions
type: meta
tags: []
---

# Vault Conventions

> Правила работы с этим vault. Источник истины — этот файл.
> Канонический design-документ: [[philosophy]].

## Frontmatter — обязательный минимум

В КАЖДОЙ заметке:

```yaml
---
title: Personal Context
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: area
tags: []
aliases: []
---
```

`updated` — обновляется автоматически плагином Update time on edit.

## Список значений `type:`

- `area` — вечно-живущий домен (work, health, family, …)
- `project` — с дедлайном/результатом
- `person` — заметка про человека
- `daily` / `weekly` / `monthly` — periodic notes
- `metrics` — health/finance ежедневные/ежемесячные записи
- `literature` — конспект внешнего источника (book / article / video / podcast / fallback)
- `permanent` — атомарная evergreen-мысль (Zettelkasten)
- `reference` — cheatsheet / snippet / рецепт
- `moc` — Map of Content (тематический индекс)
- `meta` — про сам vault (README, conventions, шаблоны)
- `decision` — ADR-стиль решение
- `meeting` — синк / 1on1 / дейли
- `pr-note` — заметка по своему PR
- `retro` — ретро по проекту/спринту/инциденту
- `incident` — пост-мортем
- `idea` — fleeting / early-stage идея

## Naming

| Что | Формат |
|---|---|
| Файлы | `kebab-case.md` |
| `title:` и H1 | Title Case с пробелами |
| Daily | `YYYY-MM-DD.md` |
| Weekly | `YYYY-Www.md` |
| Monthly | `YYYY-MM.md` |
| Health metrics | `YYYY-MM-DD.md` (внутри `10-Areas/health/metrics/`) |
| Finance monthly | `YYYY-MM.md` (внутри `10-Areas/finance/monthly/`) |
| MOC | `MOC-Rust.md`, `MOC-AI-Agents.md` |
| Permanent | имя = суть мысли, без ID/даты (`closures-vs-fn-pointers.md`) |
| People | `40-People/<name>.md` |

## Теги — фасеты, не дерево

- НЕ дублируем `type:` в тегах
- Используем для cross-cutting:
  - `#status/blocked`, `#status/needs-review`
  - `#priority/high`, `#priority/low`
  - `#domain/rust`, `#domain/frontend`, `#domain/ai`, `#domain/cs`
  - `#fleeting` — для inbox-заметок до обработки

## Wikilinks

- По умолчанию `[[basename]]` — Obsidian резолвит без указания пути
- Алиас: `[[health|здоровье]]`
- Якорь: `[[personal-context#Current state]]`
- Embed: `![[file]]` — для AI starter pack и transclusion

## Структура папок

См. [[README]] и [[philosophy]].

## Куда что класть — короткий гайд

| Хочу записать… | Куда |
|---|---|
| Идею «упало в голову» | `00-Inbox/` через QuickAdd |
| Дневную заметку | `01-Daily/daily/YYYY-MM-DD.md` (создаётся через Periodic Notes) |
| Метрику здоровья за день | `10-Areas/health/metrics/YYYY-MM-DD.md` |
| Сумму за месяц по бюджету | `10-Areas/finance/monthly/YYYY-MM.md` |
| Заметку про коллегу | `40-People/<name>.md` |
| Конспект книги/статьи/видео/подкаста | `30-Resources/` через шаблон `book/article/video/podcast` |
| Мысль про какой-то domain | `30-Resources/` через шаблон `permanent` |
| Полу-законченную идею проекта | `00-Inbox/` через шаблон `idea`, потом промоутится |
| Заметку с синка | `10-Areas/work/meetings/YYYY-MM-DD-<topic>.md` |
| Решение по архитектуре | `10-Areas/work/decisions/YYYY-MM-DD-<topic>.md` |
| PR-заметку | `10-Areas/work/prs/<pr-slug>.md` |
| Cheatsheet/рецепт | `50-Reference/` |

## Принципы

См. [[philosophy]]. Кратко: linking > folders > tags; minimum structure on start; atomic + evergreen для знаний; шаблоны для каждого типа; ритуалы review с убывающей частотой.
