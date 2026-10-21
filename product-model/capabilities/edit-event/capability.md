---
availability:
- place: desktop
references:
- kind: code
  role: implementation
  target: Panel.qml#openEditEvent
- kind: code
  role: implementation
  target: Panel.qml#submitEvent
- kind: code
  role: implementation
  target: fetch-events.py#update_event
- kind: code
  role: implementation
  target: fetch-events.py#rewrite_vevent
- kind: code
  role: implementation
  target: fetch-events.py#update_caldav_event
- kind: code
  role: implementation
  target: fetch-events.py#update_google_event
- kind: code
  role: implementation
  target: fetch-events.py#update_jmap_event
domain: agenda
---

# Edit event

Change the title, date, times or all-day setting, location and description of an event the one-day form can hold. The event stays in its calendar.
