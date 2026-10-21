---
kind: edge
routes:
  desktop: Desktop
steps:
- text: Google permanently rejects the saved sign-in while renewing access.
  kind: condition
  entities: []
  unattended: true
  contexts:
    desktop:
      place: desktop::calendar
- text: Mark the Google login as needing a reconnect.
  kind: product
  entities:
  - entity: google-login
    effect: changes
    from: Connected
    to: Reconnect needed
    facts:
    - Authorization
    - Issue
  contexts:
    desktop:
      place: desktop::calendar
---

# Mark the Google login for reconnecting

## Trigger

Google permanently rejects the saved sign-in while renewing access.

## Outcome

The login is marked as needing a reconnect, and one desktop alert says so the first time.
