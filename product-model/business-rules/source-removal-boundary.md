---
appliesTo:
- type: capability
  id: delete-calendar
- type: capability
  id: purge-calendar-data
- type: entity
  id: calendar
references:
- kind: code
  role: implementation
  target: Panel.qml#removeCalendar
- kind: code
  role: implementation
  target: fetch-events.py#forget_unused_secrets
- kind: code
  role: implementation
  target: fetch-events.py#purge_plugin_data
---

# Deleting a calendar leaves its events at the provider

Deleting a calendar removes it from Chronica, along with stored secrets no other calendar uses. Purging local data is a separate command and includes local events. Events kept by providers are never deleted by either.
