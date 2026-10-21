---
availability:
- place: shell-commands
references:
- kind: code
  role: implementation
  target: Panel.qml#nextEventSummary
- kind: code
  role: implementation
  target: BarWidget.qml
---

# Read next event

Return the next timed event today or tomorrow that has not started yet, from the loaded calendars, in the current hour cycle; empty when there is none.
