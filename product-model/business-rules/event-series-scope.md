---
appliesTo:
- type: capability
  id: edit-event
- type: capability
  id: delete-event
- type: entity
  id: event
references:
- kind: code
  role: implementation
  target: fetch-events.py#update_google_event
- kind: code
  role: implementation
  target: fetch-events.py#delete_google_event
- kind: code
  role: implementation
  target: fetch-events.py#delete_caldav_event
- kind: code
  role: implementation
  target: fetch-events.py#delete_jmap_event
- kind: code
  role: implementation
  target: Panel.qml
---

# The provider decides how far a change to a recurring event reaches

Google edits and deletes reach only the chosen occurrence. Deleting a CalDAV occurrence deletes the whole series, and the panel warns before the confirming click. A JMAP delete goes to the event the server returned, and the server decides what it means for the series.
