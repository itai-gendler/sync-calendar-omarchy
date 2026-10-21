---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Ask the clock for the timezone chooser.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::clock
- text: Open the desktop’s timezone chooser.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::clock
---

# Open the timezone chooser

## Trigger

The person asks the clock for the timezone chooser.

## Outcome

The desktop’s own timezone chooser opens; Chronica does not change the timezone itself.
