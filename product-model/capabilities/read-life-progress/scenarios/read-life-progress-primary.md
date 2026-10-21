---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Read the life progress bar.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Show age against life expectancy from the Life settings, between 0 and 100 percent.
  kind: product
  entities:
  - entity: life-settings
    effect: reads
    facts:
    - Birth year
    - Life expectancy
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Read life progress

## Trigger

A birth year is set and the person looks at the life progress bar.

## Outcome

The bar shows age, counted as the current year minus the birth year, against the life expectancy, between 0 and 100 percent.
