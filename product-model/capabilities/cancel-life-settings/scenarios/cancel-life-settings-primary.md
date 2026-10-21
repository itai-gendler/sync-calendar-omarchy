---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Cancel the birth year and life expectancy editor.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Close the editor without saving.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Discard life progress input

## Trigger

The person cancels while editing the birth year or life expectancy.

## Outcome

The editor closes and the saved values stay as they were.
