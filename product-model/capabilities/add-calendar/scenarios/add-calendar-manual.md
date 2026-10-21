---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Choose a source type (an iCalendar link, a Google ID, JMAP or local) and fill in a name and the
    fields that type needs.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
- text: Save the Calendar, enabled and in its chosen color, and sync.
  kind: product
  entities:
  - entity: calendar
    effect: creates
    facts:
    - Name
    - Source
    - Connection
    - Enabled
    - Color
    - Translation
    - Write support
    - Sync status
    - Event count
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
---

# Add a calendar by hand

## Trigger

The person chooses to add a feed by hand in Calendar Settings.

## Outcome

The new calendar is listed as enabled, and its events appear after the sync.
