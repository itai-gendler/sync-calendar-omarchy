---
availability:
- place: desktop
- place: setup
- place: google-callback
references:
- kind: code
  role: implementation
  target: google-auth.py#authorize
- kind: code
  role: implementation
  target: google-auth.py#OAuthCallbackHandler
- kind: code
  role: implementation
  target: setup.py#google_client
- kind: code
  role: implementation
  target: setup.py#reconnect_google
- kind: code
  role: implementation
  target: Panel.qml#openGoogleAuth
- kind: doc
  role: intent
  target: docs/index.html
---

# Sign in to Google

Authorize the user’s Google app for event access and calendar listing. Reconnection reuses the saved app when available and replaces the saved authorization; initial guided setup can continue to calendar selection.
