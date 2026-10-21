---
availability:
- place: desktop
- place: shell-commands
references:
- kind: code
  role: implementation
  target: Panel.qml#persistSettings
- kind: code
  role: implementation
  target: Panel.qml#setClockHourCycle
- kind: code
  role: implementation
  target: Panel.qml#setWeekStart
- kind: code
  role: implementation
  target: BarWidget.qml
---

# Change preferences

Set the hour cycle, sync interval, reminders and their timing, meeting join and first weekday. Changes apply at once and are saved with the bar’s settings.
