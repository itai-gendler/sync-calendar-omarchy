---
availability:
- place: desktop
- place: setup
references:
- kind: code
  role: implementation
  target: Panel.qml#openSetup
- kind: code
  role: implementation
  target: setup.py#setup_google
- kind: code
  role: implementation
  target: setup.py#caldav_accounts
- kind: code
  role: implementation
  target: setup.py#setup_jmap
- kind: code
  role: implementation
  target: setup.py#setup_ics
- kind: code
  role: implementation
  target: setup.py#setup_local
- kind: code
  role: implementation
  target: setup.py#save
- kind: doc
  role: intent
  target: docs/index.html
domain: calendars
---

# Connect calendar

Connect calendars through guided setup in a terminal. Google and CalDAV or iCloud accounts offer their calendars to choose from, a JMAP token or iCalendar link is checked before it is saved, and a local calendar needs only a name.
