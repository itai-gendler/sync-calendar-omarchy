---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Open Calendar Settings.
  kind: actor
  entities:
  - entity: calendar
    effect: reads
    facts: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Show the Preferences tab of Calendar Settings, and reload the configured sources.
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
  - entity: calendar
    effect: reads
    facts:
    - Name
    - Source
    - Enabled
    - Color
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::preferences
---

# Open Calendar Settings

## Trigger

The person opens Calendar Settings from the panel.

## Outcome

Calendar Settings opens on the Preferences tab, or on the tab last used while the panel has been running.
