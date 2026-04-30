---
title: Vault Rituals
type: meta
tags: []
---

# Vault Rituals

> Ритуалы review с убывающей частотой. См. [[philosophy]].

## Daily — каждый вечер (5–7 мин)

1. Открой сегодняшнюю daily-ноту (Periodic Notes → today)
2. Заполни: утренний план, сделал, узнал, inbox, хвосты, самочувствие
3. Открой `10-Areas/health/metrics/YYYY-MM-DD.md` (создастся через Templater) — заполни то, что хочешь сегодня
4. Закрой день

## Weekly — work — пятница 17:00 (15–20 мин)

1. Создай weekly-ноту через Periodic Notes (или открой текущую)
2. Перечитай daily-ноты недели
3. Заполни шаблон: что сделал, что узнал, один вопрос, энергия 1–10
4. Обнови журнал в [[work]] (добавь недельную секцию)
5. **Обнови [[work-current-week]]** — это критично для AI-context

## Weekly — health — воскресенье вечер (10 мин)

1. Открой [[health]]
2. Прочитай Dataview-ленту health-metrics за неделю (когда появится)
3. Заполни «Шаблон еженедельного ревью» в [[health]]
4. **Обнови [[current-focus]]** — топ-3 на новую неделю, блокеры, что в работе, что в parking

## Monthly — parking-lot — 29 числа (5 мин)

1. Открой [[parking-lot]]
2. Пробеги список, обнови статусы
3. Применяй правило: «вернулась в голову третий раз → запиши, не делай»

## Monthly — overall — последний день месяца (30 мин)

1. Создай monthly-ноту через Periodic Notes
2. Создай `10-Areas/finance/monthly/YYYY-MM.md` через шаблон `finance-monthly`
3. Заполни: события месяца, сдвиги стратегии, тренды веса/сна (Dataview из health/metrics), финансы
4. Что переношу на следующий месяц

## Quarterly — strategy — раз в квартал (60 мин)

1. Перечитай [[strategy]]
2. Обнови или оставь как есть
3. Раз в полгода — полный пересмотр приоритетов: что было приоритетом в окне становится в parking, что из parking — в активные на следующее окно

## Триггеры

- **Calendar плагин** — кружочки на daily/weekly/monthly, видно что не сделано
- **Tasks плагин** — повторяющиеся задачи в этом файле:

```tasks
not done
path includes _meta/rituals
```

### Recurring tasks (примеры — подставь свои даты)

> Структура повторяющейся задачи показана ниже. Замени `2030-01-01` на актуальные стартовые даты при первом прохождении.

- [ ] 🔁 every Friday at 17:00 — work weekly review 📅 2030-01-01
- [ ] 🔁 every Sunday at 21:00 — health weekly review + current-focus update 📅 2030-01-01
- [ ] 🔁 every month on 29th — parking-lot review 📅 2030-01-01
- [ ] 🔁 every month on the last day — monthly note + finance month 📅 2030-01-01
- [ ] strategy review (промежуточная сверка) 📅 2030-01-01
- [ ] strategy review (полный пересмотр приоритетов) 📅 2030-01-01
