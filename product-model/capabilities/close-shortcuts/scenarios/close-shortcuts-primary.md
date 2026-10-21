---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Dismiss the shortcuts help.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::shortcuts
- text: Close the help and show the panel again.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::shortcuts
---

# Close the shortcuts help

## Trigger

The person dismisses the keyboard shortcuts help.

## Outcome

The help closes and the calendar is shown again.
