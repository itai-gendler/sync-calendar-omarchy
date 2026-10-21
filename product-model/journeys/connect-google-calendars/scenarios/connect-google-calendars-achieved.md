---
kind: primary
result: achieved
routes:
  guided-setup: Guided setup
steps:
- text: Complete the Google sign-in in guided setup.
  kind: actor
  entities: []
  capability: sign-in-google
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: Save the Google login and offer the account’s sources.
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
  capability: sign-in-google
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: Pick the sources to add.
  kind: actor
  entities: []
  capability: connect-calendar
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: Save each chosen Calendar and sync.
  kind: product
  entities:
  - entity: calendar
    effect: creates
    facts:
    - Name
    - Source
    - Connection
    - Enabled
    - Color
    - Translation
    - Write support
    - Sync status
    - Event count
  capability: connect-calendar
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
---

# Connect Google calendars after signing in

## Trigger

The person picks Google Calendar in guided setup.

## Outcome

The chosen Google calendars are saved and synced.
