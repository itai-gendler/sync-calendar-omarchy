---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Open the keyboard shortcuts help.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::shortcuts
- text: List the navigation and action shortcuts.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::shortcuts
---

# Read the keyboard shortcuts

## Trigger

The person opens the keyboard shortcuts help.

## Outcome

The help lists the shortcuts for moving through dates and acting on events.
