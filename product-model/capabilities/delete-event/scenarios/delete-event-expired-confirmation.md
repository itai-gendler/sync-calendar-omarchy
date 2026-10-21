---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: Choose Delete once.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Disarm Delete when four seconds pass without a confirmation.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Let the delete confirmation lapse

## Trigger

The person chooses Delete once and does not confirm within four seconds.

## Outcome

Delete is disarmed and nothing is removed.
