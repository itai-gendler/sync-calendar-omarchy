---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: The sync interval elapses.
  kind: condition
  entities:
  - entity: preferences
    effect: reads
    facts:
    - Sync interval
  unattended: true
  contexts:
    desktop:
      place: desktop::calendar
- text: Fetch every enabled Calendar and read its Event entries.
  kind: product
  entities:
  - entity: calendar
    effect: changes
    facts:
    - Sync status
    - Event count
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
  contexts:
    desktop:
      place: desktop::calendar
---

# Sync at the chosen interval

## Trigger

The sync interval elapses.

## Outcome

The same sync runs on its own at the chosen interval while the panel is loaded, open or not.
