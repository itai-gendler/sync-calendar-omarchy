---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Close the panel.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Close the panel, discarding any unsaved input.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Close the panel from the clock

## Trigger

The person closes the panel from the clock.

## Outcome

The panel closes, and any unsaved event, settings or life progress input is discarded.
