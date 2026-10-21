---
appliesTo:
- type: entity
  id: event
  effect: changes
  facts:
  - Calendar
references:
- kind: code
  role: implementation
  target: Panel.qml#submitEvent
- kind: code
  role: implementation
  target: fetch-events.py#update_event
permits: []
---

# An edited event stays in its calendar

Editing keeps the event’s calendar and identity. Moving an event to another calendar is not an edit.
