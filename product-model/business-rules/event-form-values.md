---
appliesTo:
- type: capability
  id: create-event
- type: capability
  id: edit-event
references:
- kind: code
  role: implementation
  target: Panel.qml#submitEvent
- kind: code
  role: implementation
  target: Model.js#parseTimeInput
- kind: code
  role: implementation
  target: Model.js#parseDateInput
---

# A saved event describes one real day

The form needs a title and a real date. Times must be readable, and the end must come after the start. An all-day event takes the chosen date. Title, location and description are trimmed.
