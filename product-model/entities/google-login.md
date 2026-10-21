---
references:
- kind: code
  role: implementation
  target: google-auth.py#authorize
- kind: code
  role: implementation
  target: fetch-events.py#resolve_google_access_token
- kind: code
  role: implementation
  target: fetch-events.py#google_auth_summary
singleton: true
---

# Google login

The saved Google authorization used by configured Google API calendars on this desktop.

## Information kept

- **App** — The Google client chosen by the user.
- **Authorization** — The saved grant and current access used for calls to Google.
- **Issue** — A persistent rejection of the saved grant, or no such issue.

## States

### Missing

No usable Google authorization has been saved.

### Connected

Saved authorization is available for Google access and renewal.

### Reconnect needed

Google has permanently rejected the saved authorization.
