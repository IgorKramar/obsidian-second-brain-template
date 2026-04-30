---
title: <% tp.file.title %>
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
type: monthly
month: <% tp.file.title %>
tags: []
---

# <% tp.file.title %> — месячное ревью

> Делаю в последний день месяца, 30 минут.

## Главные события месяца

- 

## Что сдвинулось по стратегии

См. [[strategy]].

- 

## Здоровье — тренды

```dataview
TABLE
  weight_kg as "Weight",
  sleep_hours as "Sleep h",
  mood as "Mood",
  energy as "Energy"
FROM "10-Areas/health/metrics"
WHERE startswith(string(date), "<% tp.file.title %>")
SORT date ASC
```

## Финансы — итоги месяца

См. [[finance/monthly/<% tp.file.title %>]] (создать через шаблон `finance-monthly`).

## Parking-lot review

См. [[parking-lot]] — пробежать, обновить статусы.

## Что переношу на следующий месяц

- 
