---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: Choose Reconnect Google account.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
- text: Sign in again at Google with the saved app.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: setup
- text: Return the result of the consent.
  kind: actor
  entities: []
  actor: google-authorization
  contexts:
    desktop:
      place: google-callback
- text: Save the reconnected Google login and finish setup.
  kind: product
  entities:
  - entity: google-login
    effect: changes
    from: Reconnect needed
    to: Connected
    facts:
    - App
    - Authorization
    - Issue
  actor: desktop-user
  contexts:
    desktop:
      place: setup
---

# Reconnect Google from the panel

## Trigger

The person chooses to reconnect a Google calendar in Calendar Settings.

## Outcome

The new sign-in replaces the saved one, clears the login problem and syncs; no calendar is added twice.
