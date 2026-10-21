---
availability:
- place: desktop
references:
- kind: code
  role: implementation
  target: Panel.qml#openExternalUrl
- kind: code
  role: implementation
  target: fetch-events.py#extract_meeting_info
- kind: code
  role: implementation
  target: fetch-events.py#fetch_google_api_calendar
- kind: code
  role: implementation
  target: fetch-events.py#fetch_jmap_calendar
domain: agenda
---

# Join meeting

Open an event’s Google Meet, Zoom, Teams, Webex or Jitsi link, or a meeting address its provider supplies, with the desktop’s handler. The Join button shows while meeting join is on.
