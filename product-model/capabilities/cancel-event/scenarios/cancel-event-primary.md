---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Cancel the open form.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: Close the form without saving anything.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
---

# Discard the event form

## Trigger

The person cancels while creating or editing an event.

## Outcome

Nothing is saved, and events saved earlier are unchanged.
