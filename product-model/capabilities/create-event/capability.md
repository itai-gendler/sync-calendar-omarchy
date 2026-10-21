---
availability:
- place: desktop
references:
- kind: code
  role: implementation
  target: Panel.qml#openAddEvent
- kind: code
  role: implementation
  target: Panel.qml#applyQuickAdd
- kind: code
  role: implementation
  target: Panel.qml#submitEvent
- kind: code
  role: implementation
  target: fetch-events.py#create_event
- kind: code
  role: implementation
  target: fetch-events.py#create_local_event
- kind: code
  role: implementation
  target: fetch-events.py#create_google_event
- kind: code
  role: implementation
  target: fetch-events.py#create_caldav_event
- kind: code
  role: implementation
  target: fetch-events.py#create_jmap_event
domain: agenda
---

# Create event

Create a timed or all-day event on one day, in a calendar Chronica can write to. Quick Add fills the form from a sentence, and the person still reviews and saves.

New events have no recurrence. The form starts at 09:00–10:00 on the selected day, in the first writable calendar. Quick Add reads English and French dates and times; a single time gets one hour.
