---
appliesTo:
- type: entity
  id: event
  effect: changes
  contexts:
  - place: desktop::event-editor
references:
- kind: code
  role: implementation
  target: fetch-events.py#sync_all_events
- kind: code
  role: implementation
  target: Panel.qml#openEditEvent
permits:
- actors:
  - desktop-user
  when:
  - fact: Editable
    is: true
---

# Only the desktop user edits events the one-day form can hold

An event offers Edit when it is writable, fits the one-day form and is not part of a CalDAV or JMAP recurring series. Each occurrence of a recurring Google event can be edited on its own. Where editing is not supported, the panel offers no Edit.
