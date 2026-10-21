---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Pick a date or move to another day, week, month or year.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Show the month from the chosen first weekday, with ISO week numbers, today, the selected date
    and the days holding Event entries.
  kind: product
  entities:
  - entity: event
    effect: reads
    facts:
    - Start
    - End
    - Calendar
  - entity: preferences
    effect: reads
    facts:
    - Week start
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Browse the month grid

## Trigger

The person picks a date, moves by day, week, month or year, jumps to the start or end of a week or month, or returns to today.

## Outcome

The grid shows the month from the chosen first weekday, with ISO week numbers, today, the selected date and a mark on each day that has events.
