---
availability:
- place: desktop
references:
- kind: code
  role: implementation
  target: Panel.qml#checkUpcomingNotifications
- kind: code
  role: implementation
  target: Model.js#notificationStage
- kind: code
  role: implementation
  target: Model.js#dueNotifications
- kind: code
  role: implementation
  target: fetch-events.py#notify_command
domain: agenda
---

# Send reminders

Send desktop reminders before timed events while reminders are on, including events just after midnight. The desktop’s notification service delivers them.
