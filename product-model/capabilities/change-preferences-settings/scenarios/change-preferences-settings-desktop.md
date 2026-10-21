---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Choose new clock, sync, reminder, meeting join or first weekday values.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::preferences
- text: Apply and save the Preferences.
  kind: product
  entities:
  - entity: preferences
    effect: changes
    facts:
    - Hour cycle
    - Clock format
    - Sync interval
    - Notifications
    - Reminder timing
    - Meeting join
    - Week start
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::preferences
---

# Change preferences

## Trigger

The person changes a value on the Preferences tab of Calendar Settings.

## Outcome

The new value applies at once and is saved. Manual stops the sync interval timer, and a new hour cycle reformats times without fetching events again.
