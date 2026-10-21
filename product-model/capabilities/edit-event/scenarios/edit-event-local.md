---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Change the form fields and save.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: Rewrite the local Event, keeping its identity and creation time.
  kind: product
  entities:
  - entity: event
    effect: changes
    facts:
    - Title
    - Start
    - End
    - All day
    - Location
    - Description
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
---

# Edit a local event

## Trigger

The person saves changes to a local event.

## Outcome

The event keeps its calendar, identity and creation time; a sync is requested and the form closes.
