---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Select a date and, optionally, one source’s filter chip.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: List the day’s Event entries with the name and color of their Calendar.
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
  - entity: calendar
    effect: reads
    facts:
    - Name
    - Color
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Read the selected day

## Trigger

The person selects a date, optionally narrowing the agenda to one calendar with its filter chip.

## Outcome

All-day events come first, then timed events by start time and title. A day without events shows as empty.
