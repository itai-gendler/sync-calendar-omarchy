---
appliesTo:
- type: capability
  id: sync-calendars
- type: capability
  id: change-preferences-settings
- type: entity
  id: preferences
references:
- kind: code
  role: implementation
  target: Panel.qml#syncCalendars
- kind: code
  role: implementation
  target: Panel.qml
- kind: code
  role: implementation
  target: Backend.qml#call
- kind: code
  role: implementation
  target: fetch-events.py#serve
---

# Manual turns off only the interval sync

Opening the panel syncs unless it synced in the last 30 seconds. Sync, a changed calendar list and every saved or deleted event still sync. The interval is 15 minutes by default. Syncs and edits from the panel run one at a time, in order.
