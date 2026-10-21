---
appliesTo:
- type: entity
  id: event
- type: capability
  id: send-reminders
references:
- kind: code
  role: implementation
  target: Model.js#dueNotifications
---

# Event reminders say only when something starts

A reminder says that an event starts now or in a number of minutes, and points to the panel. It never includes the event’s title, location or calendar.
