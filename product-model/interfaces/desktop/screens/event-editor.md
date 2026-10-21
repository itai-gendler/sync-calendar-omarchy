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
  collects:
  - Title
  - Start
  - End
  - All day
  - Location
  - Description
  - Calendar
- entity: calendar
  shows:
  - Name
  - Color
  - Write support
references:
- kind: code
  role: implementation
  target: Panel.qml#openAddEvent
- kind: code
  role: implementation
  target: Panel.qml#openEditEvent
- kind: code
  role: implementation
  target: Panel.qml#submitEvent
---

# Event editor

Creating or editing one event, including filling it from a Quick Add sentence and correcting it before saving.
