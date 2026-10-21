---
entities:
- entity: calendar
  shows:
  - Name
  - Source
  - Enabled
  - Color
  collects:
  - Name
  - Source
  - Connection
  - Color
- entity: google-login
  shows:
  - Issue
references:
- kind: code
  role: implementation
  target: Panel.qml#commitNewCalendar
- kind: code
  role: implementation
  target: Panel.qml#toggleCalendarEnabled
- kind: code
  role: implementation
  target: Panel.qml#openSetup
---

# Calendars

The Calendars tab of Calendar Settings: the configured calendars and their controls, and the form for adding one by hand.
