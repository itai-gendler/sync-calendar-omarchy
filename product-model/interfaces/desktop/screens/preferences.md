---
entities:
- entity: preferences
  shows:
  - Hour cycle
  - Clock format
  - Sync interval
  - Notifications
  - Reminder timing
  - Meeting join
  - Week start
  collects:
  - Hour cycle
  - Clock format
  - Sync interval
  - Notifications
  - Reminder timing
  - Meeting join
  - Week start
references:
- kind: code
  role: implementation
  target: Panel.qml#persistSettings
---

# Preferences

The Preferences tab of Calendar Settings: hour cycle, sync interval, reminders, meeting join and first weekday.
