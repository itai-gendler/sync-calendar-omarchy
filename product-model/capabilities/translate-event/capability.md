---
availability:
- place: desktop
references:
- kind: code
  role: implementation
  target: fetch-events.py#translate_korean_to_english
- kind: code
  role: implementation
  target: fetch-events.py#parse_ics
- kind: code
  role: implementation
  target: fetch-events.py#fetch_google_api_calendar
domain: agenda
---

# Translate event

When a calendar has translation turned on, translate Korean titles and locations into English through Google Translate while syncing. Descriptions stay as written.
