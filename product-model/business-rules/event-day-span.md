---
appliesTo:
- type: entity
  id: event
references:
- kind: code
  role: implementation
  target: fetch-events.py#expand_multiday_event
---

# A multi-day event appears on each date it covers

All-day end dates are exclusive. A timed event ending exactly at midnight does not appear on the next day. Each day shows the event’s full time span.
