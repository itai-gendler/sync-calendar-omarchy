---
kind: edge
routes:
  desktop: Desktop
steps:
- text: Confirm Delete.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Show the failure with the Event title.
  kind: product
  entities:
  - entity: event
    effect: reads
    facts:
    - Title
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Report a failed delete

## Trigger

The provider refuses the delete, or the event can no longer be found.

## Outcome

The agenda shows the failure with the event’s title; nothing is reported as deleted.
