---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: Switch to the next 7 days, optionally with a filter chip.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: List the matching Event entries under a heading per day.
  kind: product
  entities:
  - entity: event
    effect: reads
    facts:
    - Title
    - Start
    - End
    - All day
    - Location
    - Description
    - Calendar
    - Recurrence
    - Meeting link
    - Writable
    - Editable
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Read the next 7 days

## Trigger

The person switches the agenda to the next 7 days.

## Outcome

The list starts today and covers seven days, with a heading for each day that has events. Selecting a date switches back to that day.
