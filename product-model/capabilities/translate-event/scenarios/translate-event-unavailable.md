---
kind: edge
routes:
  desktop: Desktop
steps:
- text: A translation request fails.
  kind: condition
  entities: []
  unattended: true
  contexts:
    desktop:
      place: desktop::calendar
- text: Keep the original Event title and location.
  kind: product
  entities:
  - entity: event
    effect: reads
    facts:
    - Title
    - Location
  contexts:
    desktop:
      place: desktop::calendar
---

# Keep the text when translation is unavailable

## Trigger

The translator fails or returns nothing usable.

## Outcome

The original title and location stay readable.
