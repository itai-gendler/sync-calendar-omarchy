---
type: cli
actors:
- desktop-user
references:
- kind: code
  role: implementation
  target: setup.py
- kind: code
  role: implementation
  target: google-auth.py
- kind: code
  role: implementation
  target: fetch-events.py#purge_plugin_data
---

# Guided setup and cleanup

The supported terminal workflow for connecting calendars, signing in to Google and removing saved calendar data. Provider websites remain external dependencies.
