---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Choose to disable a configured source.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
- text: Mark the Calendar disabled and sync.
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

# Disable a calendar

## Trigger

The person chooses Disable calendar in Calendar Settings.

## Outcome

The calendar stays configured but is left out of syncing, so its events leave the agenda.
