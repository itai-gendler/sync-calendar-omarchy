---
actors:
- desktop-user
references:
- kind: code
  role: implementation
  target: setup.py#setup_google
- kind: code
  role: implementation
  target: google-auth.py#authorize
---

# Connect Google calendars

## Goal

Sign in to Google in guided setup and add the account's calendars.

## Success criterion

The chosen Google calendars are saved and synced.
