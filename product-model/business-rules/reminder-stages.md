---
appliesTo:
- type: entity
  id: event
- type: entity
  id: preferences
- type: capability
  id: send-reminders
references:
- kind: code
  role: implementation
  target: Model.js#notificationStage
- kind: code
  role: implementation
  target: Model.js#dueNotifications
- kind: code
  role: implementation
  target: Panel.qml#checkUpcomingNotifications
---

# A timed event gets at most one reminder per stage while the panel runs

Staged timing uses the current 10-, 5- or 1-minute stage; a single interval uses the chosen number of minutes. Checks run every 30 seconds, each minute and after each sync. Stages already sent are remembered while the panel runs. All-day events get no reminder.

The time to start is rounded to whole minutes. A check that finds an event already in a later stage sends that stage.
