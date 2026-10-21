---
appliesTo:
- type: capability
  id: browse-agenda
- type: capability
  id: copy-agenda
- type: entity
  id: event
references:
- kind: code
  role: implementation
  target: fetch-events.py#sync_all_events
- kind: code
  role: implementation
  target: Panel.qml
---

# All-day events come before timed events

Within a date, all-day events come first, then timed events by local start time and title. A filter chip narrows the agenda to one calendar without changing what is synced.
