---
kind: edge
routes:
  desktop: Desktop
steps:
- text: Request a sync.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Read the Event entries of each Calendar that answers and record each result on its own.
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

# Sync the other calendars when one fails

## Trigger

One calendar fails to sync while the others succeed.

## Outcome

The calendars that synced show their events, the failed calendar shows its error, and local events never depend on a provider.
