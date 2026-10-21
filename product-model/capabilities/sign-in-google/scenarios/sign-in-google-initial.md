---
kind: primary
routes:
  guided-setup: Guided setup
steps:
- text: Reuse a saved Google app, take the newest client file in Downloads, or enter the app’s client
    ID and secret.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: Open Google’s consent page and wait for the answer.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: Return the result of the consent.
  kind: actor
  entities: []
  actor: google-authorization
  contexts:
    guided-setup:
      place: google-callback
- text: Exchange the returned code and save the Google login.
  kind: product
  entities:
  - entity: google-login
    effect: changes
    from: Missing
    to: Connected
    facts:
    - App
    - Authorization
    - Issue
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
---

# Sign in to Google for the first time

## Trigger

The person starts Google setup with no saved login.

## Outcome

The Google login is saved and setup goes on to choosing calendars.
