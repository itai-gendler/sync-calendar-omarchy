---
entities:
- entity: event
  shows:
  - Title
  - Start
  - End
  - All day
  - Location
  - Description
  - Calendar
  - Recurrence
  - Meeting link
  - Writable
  - Editable
- entity: calendar
  shows:
  - Name
  - Color
  - Sync status
  - Event count
- entity: preferences
  shows:
  - Hour cycle
  - Week start
- entity: life-settings
  shows:
  - Birth year
  - Life expectancy
  collects:
  - Birth year
  - Life expectancy
- entity: google-login
  shows:
  - Issue
references:
- kind: code
  role: implementation
  target: Panel.qml
- kind: code
  role: implementation
  target: Model.js#upcomingEvents
---

# Calendar

The month, the agenda for the selected day or the next 7 days, event details, and progress through the year and life.
