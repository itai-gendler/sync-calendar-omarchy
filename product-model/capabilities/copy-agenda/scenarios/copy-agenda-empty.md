---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: Copy the agenda while it is empty.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Leave the clipboard unchanged.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Copy an empty agenda

## Trigger

The person copies the agenda while it is empty.

## Outcome

Nothing is copied and the clipboard keeps what it held.
