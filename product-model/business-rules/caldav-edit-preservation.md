---
appliesTo:
- type: entity
  id: event
  effect: changes
  facts:
  - Title
  - Start
  - End
  - All day
  - Location
  - Description
references:
- kind: code
  role: implementation
  target: fetch-events.py#rewrite_vevent
- kind: code
  role: implementation
  target: fetch-events.py#update_caldav_event
---

# CalDAV edits preserve unedited event content and report version conflicts

Saving replaces only the fields the form owns and keeps alarms, attendees and the rest of the event. When the server says the event changed elsewhere, nothing is overwritten, and the person refreshes and edits again. Recurring CalDAV events are not edited from the panel.
