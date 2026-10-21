---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: Choose Delete, then confirm while it is armed.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Warn that every occurrence will be deleted, then delete the Event’s whole series, found by its
    UID if needed.
  kind: product
  entities:
  - entity: event
    effect: removes
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Delete a recurring CalDAV event

## Trigger

The person deletes one occurrence of a recurring event from a CalDAV calendar.

## Outcome

After the second click within four seconds the whole series is deleted, and the next sync updates the agenda.
