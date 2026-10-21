---
appliesTo:
- type: entity
  id: calendar
- type: capability
  id: connect-calendar
references:
- kind: code
  role: implementation
  target: setup.py#add_entries
- kind: code
  role: implementation
  target: setup.py#setup_google
- kind: code
  role: implementation
  target: setup.py#caldav_accounts
---

# Guided setup gives added sources distinct names

Guided setup omits already configured Google IDs and CalDAV collection addresses and adds numbered suffixes to names already used, comparing names without case. It replaces the untouched empty sample entry.
