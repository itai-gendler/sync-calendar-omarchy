---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Put the life progress bar away.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Clear the Life settings birth year, keeping the life expectancy.
  kind: product
  entities:
  - entity: life-settings
    effect: changes
    facts:
    - Birth year
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Put life progress away

## Trigger

The person puts the life progress bar away.

## Outcome

The birth year is cleared and the bar is hidden; the chosen life expectancy is kept for next time.
