---
appliesTo:
- type: entity
  id: calendar
- type: entity
  id: event
references:
- kind: code
  role: implementation
  target: fetch-events.py#sync_all_events
- kind: code
  role: implementation
  target: fetch-events.py#fetch_caldav_calendar
- kind: code
  role: implementation
  target: fetch-events.py#fetch_jmap_calendar
---

# The agenda covers recent and coming weeks

A sync asks for about 45 days before and 90 days after now. Saved provider answers may cover a longer look-ahead so they can be reused. Chronica is not an archive of older events.
