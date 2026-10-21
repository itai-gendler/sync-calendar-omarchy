---
kind: edge
routes:
  desktop: Desktop
steps:
- text: Save the edits.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: The CalDAV server reports that the Event was changed elsewhere.
  kind: condition
  entities:
  - entity: event
    effect: reads
    facts: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: Report the change made elsewhere and keep the form open.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
---

# Report a change made on another device

## Trigger

The CalDAV server refuses the save because the event was changed elsewhere.

## Outcome

The newer version is kept; the form stays open and asks the person to refresh and edit again.
