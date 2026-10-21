---
kind: primary
routes:
  guided-setup: Guided setup
steps:
- text: Run the data purge.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: Remove the stored local Event entries and the Google login.
  kind: product
  actor: desktop-user
  entities:
  - entity: event
    effect: removes
  - entity: google-login
    effect: changes
    from: Connected
    to: Missing
    facts:
    - App
    - Authorization
    - Issue
  contexts:
    guided-setup:
      place: setup
- text: Remove every Calendar and the downloaded data, leaving provider data untouched.
  kind: product
  actor: desktop-user
  entities:
  - entity: calendar
    effect: removes
  contexts:
    guided-setup:
      place: setup
---

# Purge all stored calendar data

## Trigger

The person runs the data purge from a terminal.

## Outcome

The stored calendar files and their keyring items are removed where present, the command lists what it removed, and events at the providers are untouched.
