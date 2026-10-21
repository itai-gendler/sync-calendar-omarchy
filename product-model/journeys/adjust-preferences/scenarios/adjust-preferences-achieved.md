---
kind: primary
result: achieved
routes:
  desktop: Desktop
steps:
- text: Open the settings from the panel.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
  capability: open-calendar-settings
- text: Show the Preferences tab.
  kind: product
  entities:
  - entity: preferences
    effect: reads
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
  capability: open-calendar-settings
- text: Choose a new sync interval or reminder timing.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::preferences
  capability: change-preferences-settings
- text: Apply and save the Preferences.
  kind: product
  actor: desktop-user
  entities:
  - entity: preferences
    effect: changes
    facts:
    - Sync interval
    - Reminder timing
  contexts:
    desktop:
      place: desktop::preferences
  capability: change-preferences-settings
---

# Adjust preferences from the panel

## Trigger

The person opens Calendar Settings to change how the clock, syncing or reminders behave.

## Outcome

The changed preference is in effect and saved.
