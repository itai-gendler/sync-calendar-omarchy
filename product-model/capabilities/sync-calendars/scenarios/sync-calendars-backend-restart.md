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
- text: Fail the waiting requests and restart the helper for later ones.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Recover when the background helper stops

## Trigger

The background helper stops while requests are waiting.

## Outcome

Waiting requests fail with a message, the helper restarts after a delay that doubles up to one minute, and a failed save is not replayed.
