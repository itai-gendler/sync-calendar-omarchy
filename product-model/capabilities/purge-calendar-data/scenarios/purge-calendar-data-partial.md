---
kind: edge
routes:
  guided-setup: Guided setup
steps:
- text: Run the data purge.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: List the removed files and the failures.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
---

# Report an incomplete purge

## Trigger

Some stored files cannot be removed.

## Outcome

The command lists what it removed and what failed, without claiming that everything is gone.
