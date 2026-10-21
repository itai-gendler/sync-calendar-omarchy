---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Choose to delete a configured source.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
- text: Remove the Calendar from Chronica, clear stored secrets no other source uses, and sync.
  kind: product
  entities:
  - entity: calendar
    effect: removes
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
---

# Delete a calendar

## Trigger

The person deletes a calendar in Calendar Settings.

## Outcome

The calendar and its events leave the panel; the events at the provider are untouched.
