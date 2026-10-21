---
kind: edge
routes:
  desktop: Desktop
steps:
- text: Save the edits to a remote source.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: Show the failure in the form and keep the edits.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
---

# Keep the edits when the provider refuses

## Trigger

Saving to a remote calendar fails on the network or is refused by the provider.

## Outcome

The form stays open with the error and the edits, ready to correct or retry; nothing is queued to send later.
