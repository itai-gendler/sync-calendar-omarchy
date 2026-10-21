---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Ask the clock for its next format.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::clock
- text: Change Preferences to the next distinct format and its hour cycle.
  kind: product
  entities:
  - entity: preferences
    effect: changes
    facts:
    - Clock format
    - Hour cycle
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::clock
---

# Cycle the clock format from the bar

## Trigger

The person asks the clock for its next format.

## Outcome

The clock shows the next format at once, with its hour cycle, and keeps it from then on when the bar can save its settings.
