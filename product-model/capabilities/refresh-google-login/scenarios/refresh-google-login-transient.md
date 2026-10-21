---
kind: edge
routes:
  desktop: Desktop
steps:
- text: Renewing Google access meets a temporary network or server failure.
  kind: condition
  entities: []
  unattended: true
  contexts:
    desktop:
      place: desktop::calendar
- text: Keep the saved Google login and report the failed sync.
  kind: product
  entities:
  - entity: google-login
    effect: reads
    facts:
    - App
    - Authorization
    - Issue
  contexts:
    desktop:
      place: desktop::calendar
---

# Keep the Google login after a temporary failure

## Trigger

Renewing access meets a network or server failure.

## Outcome

The calendar reports a sync error; the login is not marked for reconnecting and no alert is sent.
