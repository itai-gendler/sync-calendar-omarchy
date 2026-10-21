---
appliesTo:
- type: entity
  id: event
- type: entity
  id: preferences
references:
- kind: code
  role: implementation
  target: fetch-events.py#parse_datetime_value
- kind: code
  role: implementation
  target: fetch-events.py#expand_recurring_event
- kind: code
  role: implementation
  target: Model.js#formatEventTime
---

# Event times use the desktop time zone and the hour preference

Times with a time zone are converted to desktop local time; floating times keep their wall-clock values. A recurring event is expanded in its own time zone before conversion, so a daylight-saving change on the desktop does not shift the series. The hour cycle changes how times are shown and copied, never the stored times.
