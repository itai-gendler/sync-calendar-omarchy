---
availability:
- place: desktop
references:
- kind: code
  role: implementation
  target: Panel.qml#syncCalendars
- kind: code
  role: implementation
  target: Backend.qml#call
- kind: code
  role: implementation
  target: fetch-events.py#sync_all_events
- kind: code
  role: implementation
  target: fetch-events.py#fetch_calendar
- kind: code
  role: implementation
  target: fetch-events.py#fetch_google_api_calendar
- kind: code
  role: implementation
  target: fetch-events.py#fetch_jmap_calendar
- kind: code
  role: implementation
  target: fetch-events.py#fetch_caldav_calendar
domain: calendars
---

# Sync calendars

Fetch every enabled calendar, and local events, into the agenda. Syncs run when the panel opens, on Sync, at the chosen interval, when the calendar list changes and after each saved or deleted event. Providers’ change information lets unchanged results be reused.
