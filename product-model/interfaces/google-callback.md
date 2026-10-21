---
type: webhook
actors:
- google-authorization
references:
- kind: code
  role: implementation
  target: google-auth.py#OAuthCallbackHandler
---

# Google sign-in callback

The local return contract for a Google sign-in already initiated by the desktop user. It completes that authorization run.
