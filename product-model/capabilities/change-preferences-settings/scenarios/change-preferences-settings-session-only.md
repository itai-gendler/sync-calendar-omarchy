---
kind: edge
routes:
  desktop: Desktop
steps:
- text: Choose a new value.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::preferences
- text: Apply the Preferences for this session.
  kind: product
  entities:
  - entity: preferences
    effect: changes
    facts:
    - Hour cycle
    - Sync interval
    - Notifications
    - Reminder timing
    - Meeting join
    - Week start
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::preferences
---

# Change preferences the bar cannot save

## Trigger

Chronica is not placed in the bar layout, so the host cannot save its settings.

## Outcome

The new values apply until the panel restarts.
