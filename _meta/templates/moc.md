---
title: MOC — 
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
type: moc
tags: [domain/]
---

# 

> Тематический индекс. Ручные ссылки на ключевые ноты + Dataview для всего остального.

## Корневые материалы

- 

## Permanent notes

```dataview
LIST
FROM #domain/ AND ("type" = "permanent")
SORT file.mtime DESC
```

## Литературные конспекты

```dataview
TABLE source_type as "Type", author, year
FROM #domain/ AND ("type" = "literature")
SORT file.mtime DESC
```

## Все заметки по теме (auto)

```dataview
LIST
FROM #domain/
SORT file.mtime DESC
```
