---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Read the clock.
  kind: actor
  entities:
  - entity: preferences
    effect: reads
    facts:
    - Hour cycle
    - Clock format
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::clock
- text: Show the current local date and time in the Preferences format and hour cycle.
  kind: product
  entities:
  - entity: preferences
    effect: reads
    facts:
    - Hour cycle
    - Clock format
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::clock
---

# Read the clock

## Trigger

The person looks at the clock in the bar.

## Outcome

The bar shows the current local date and time in the saved format and hour cycle.
