---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Ask for the next color on a configured source.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
- text: Save the new Calendar color and sync.
  kind: product
  entities:
  - entity: calendar
    effect: changes
    facts:
    - Color
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
---

# Change a calendar’s color

## Trigger

The person changes a calendar’s color in Calendar Settings.

## Outcome

The calendar takes the next color of the palette, and its events and day marks use it.
