---
availability:
- place: setup
references:
- kind: code
  role: implementation
  target: fetch-events.py#purge_plugin_data
---

# Purge calendar data

Remove all of Chronica’s stored data from a terminal: the calendar list, the Google login, local events, downloaded events and caches, and their keyring items. Calendars at the providers are untouched.
