---
actors:
- desktop-user
references:
- kind: code
  role: implementation
  target: Panel.qml#quickAdd
- kind: code
  role: implementation
  target: Panel.qml#submitEvent
---

# Save an event from a shell command

## Goal

Start an event from a key binding or script, then review and save it in the panel.

## Success criterion

The reviewed event is saved in the chosen calendar.
