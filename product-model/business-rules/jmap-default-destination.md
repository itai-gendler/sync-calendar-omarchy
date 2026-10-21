---
appliesTo:
- type: entity
  id: calendar
- type: capability
  id: connect-calendar
- type: capability
  id: create-event
references:
- kind: code
  role: implementation
  target: fetch-events.py#fetch_jmap_calendar
- kind: code
  role: implementation
  target: fetch-events.py#jmap_default_calendar
- kind: code
  role: implementation
  target: fetch-events.py#create_jmap_event
---

# An unspecified JMAP destination uses the default writable calendar

When the entry names no calendar, syncing reads events from all of the account’s calendars, while a new event goes to the account’s default calendar, or to its first writable one when none is the default. An entry that names a calendar reads and creates there.
