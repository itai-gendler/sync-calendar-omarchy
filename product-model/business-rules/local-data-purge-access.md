---
appliesTo:
- type: entity
  id: event
  effect: removes
  contexts:
  - place: setup
permits:
- actors:
  - desktop-user
references:
- kind: code
  role: implementation
  target: fetch-events.py#purge_plugin_data
---

# Only the desktop user purges local event data

The purge command removes stored local events. It never deletes events kept by a provider.
