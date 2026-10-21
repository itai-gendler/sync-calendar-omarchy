---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Select the open Event again.
  kind: actor
  entities:
  - entity: event
    effect: reads
    facts:
    - Title
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Close its details and keep the agenda.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Hide an event’s details

## Trigger

The person selects the open event again.

## Outcome

Its details close and the agenda stays where it was.
