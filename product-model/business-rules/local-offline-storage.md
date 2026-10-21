---
appliesTo:
- type: entity
  id: event
- type: capability
  id: create-event
- type: capability
  id: edit-event
- type: capability
  id: delete-event
references:
- kind: code
  role: implementation
  target: Model.js#getWritableCalendars
- kind: code
  role: implementation
  target: fetch-events.py#create_local_event
- kind: code
  role: implementation
  target: fetch-events.py#update_local_event
- kind: code
  role: implementation
  target: fetch-events.py#delete_local_event
- kind: code
  role: implementation
  target: fetch-events.py#sync_all_events
---

# Local events stay on this machine

Creating, editing and deleting local events changes the local store, with no account or network. A Local Calendar is offered for new events even when none is configured, and its stored events then appear in the agenda.
