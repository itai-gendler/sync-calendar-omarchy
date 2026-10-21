---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Choose to enable a disabled source.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
- text: Mark the Calendar enabled and sync.
  kind: product
  entities:
  - entity: calendar
    effect: changes
    facts:
    - Enabled
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
---

# Enable a calendar

## Trigger

The person chooses Enable calendar on a disabled calendar in Calendar Settings.

## Outcome

The calendar is synced again and its events return to the agenda.
