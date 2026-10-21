---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Open the panel from the clock.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::clock
- text: Show the panel at today, reload saved data and sync if due.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Open the panel from the clock

## Trigger

The person opens the panel from the clock.

## Outcome

The panel shows today and reloads the saved events, and it syncs unless it synced in the last 30 seconds.
