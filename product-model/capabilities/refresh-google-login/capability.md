---
availability:
- place: desktop
references:
- kind: code
  role: implementation
  target: fetch-events.py#resolve_google_access_token
- kind: code
  role: implementation
  target: fetch-events.py#_record_google_refresh_error
---

# Refresh Google login

Renew Google access when a sync or a write needs it. Access that is still valid is reused, and a temporary failure is kept apart from a sign-in Google has rejected.
