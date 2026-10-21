---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Read the year progress bar.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Show completed days divided by the days in the year, as a rounded percentage.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Read year progress

## Trigger

The person looks at the year progress bar in the panel.

## Outcome

The bar shows the share of today’s year already completed in whole days, as a rounded percentage.
