---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Choose Sync.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Fetch every enabled Calendar and read its Event entries into the agenda.
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
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Sync now

## Trigger

The person chooses Sync.

## Outcome

Each calendar’s result and the last sync time update, and the agenda shows what was fetched.
