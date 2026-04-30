---
title: MOC — Example Topic
type: moc
tags: [domain/example]
---

# Example Topic

> A Map of Content for `<topic>`. This file demonstrates the MOC pattern: a small curated index plus auto-generated lists via Dataview.
> Rename this file (e.g. `MOC-Rust.md`, `MOC-Frontend.md`) and replace `domain/example` with your actual domain tag.

## Hand-curated entry points

- 

## Permanent notes

```dataview
LIST
FROM #domain/example AND ("type" = "permanent")
SORT file.mtime DESC
```

## Literature notes

```dataview
TABLE source_type as "Type", author, year
FROM #domain/example AND ("type" = "literature")
SORT file.mtime DESC
```

## All notes on this topic (auto)

```dataview
LIST
FROM #domain/example
SORT file.mtime DESC
```
