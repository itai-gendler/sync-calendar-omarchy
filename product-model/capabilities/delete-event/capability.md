---
availability:
- place: desktop
references:
- kind: code
  role: implementation
  target: Panel.qml#requestDelete
- kind: code
  role: implementation
  target: fetch-events.py#delete_event
- kind: code
  role: implementation
  target: fetch-events.py#delete_caldav_event
- kind: code
  role: implementation
  target: fetch-events.py#delete_google_event
- kind: code
  role: implementation
  target: fetch-events.py#delete_jmap_event
domain: agenda
---

# Delete event

Delete a writable event with a second, confirming click. Deleting an occurrence of a recurring CalDAV event deletes the whole series.
