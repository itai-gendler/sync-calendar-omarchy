---
appliesTo:
- type: entity
  id: event
  effect: removes
  contexts:
  - place: desktop::calendar
references:
- kind: code
  role: implementation
  target: Panel.qml
- kind: code
  role: implementation
  target: fetch-events.py#fetch_google_api_calendar
- kind: code
  role: implementation
  target: fetch-events.py#resolve_event_target
permits:
- actors:
  - desktop-user
  when:
  - fact: Writable
    is: true
---

# Only the desktop user deletes events the panel marks writable

The agenda offers Delete for events whose calendar allows writing. Events from a Google calendar the account can only read, and from iCalendar links, have no Delete. The provider makes the final decision.
