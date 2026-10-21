---
appliesTo:
- type: entity
  id: google-login
- type: capability
  id: sign-in-google
- type: capability
  id: refresh-google-login
references:
- kind: code
  role: implementation
  target: fetch-events.py#resolve_google_access_token
- kind: code
  role: implementation
  target: fetch-events.py#_record_google_refresh_error
- kind: code
  role: implementation
  target: google-auth.py#authorize
---

# Transient Google failures do not mean the saved grant was revoked

Permanent token rejection records a reconnect issue and produces one disconnect alert for that newly recorded issue. Temporary transport or server failure reports a source error without marking permanent revocation. Successful authorization or renewal clears the persistent issue.
