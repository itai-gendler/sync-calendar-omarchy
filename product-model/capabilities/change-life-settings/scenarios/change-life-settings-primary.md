---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Enter a birth year and an expected lifespan and confirm.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Save the Life settings.
  kind: product
  entities:
  - entity: life-settings
    effect: changes
    facts:
    - Birth year
    - Life expectancy
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Set the birth year and life expectancy

## Trigger

The person opens the life progress editor and enters a birth year and an expected lifespan.

## Outcome

Life progress uses the new values. A birth year outside the last 120 years leaves it unset, and a lifespan outside 1 to 150 years falls back to 90.
