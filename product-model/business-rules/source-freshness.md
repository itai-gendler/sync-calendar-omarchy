---
appliesTo:
- type: entity
  id: calendar
- type: capability
  id: sync-calendars
references:
- kind: code
  role: implementation
  target: fetch-events.py#fetch_calendar
- kind: code
  role: implementation
  target: fetch-events.py#fetch_google_api_calendar
- kind: code
  role: implementation
  target: fetch-events.py#fetch_caldav_calendar
- kind: code
  role: implementation
  target: fetch-events.py#fetch_jmap_calendar
---

# Unchanged provider data may be reused after a freshness check

iCalendar links use ETag or modification time, Google can reuse a one-page event list, CalDAV checks the collection tag, and JMAP checks for event changes. Reusing a result still needs a successful check with the source.
