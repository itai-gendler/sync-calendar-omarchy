---
kind: alternative
routes:
  guided-setup: Guided setup
steps:
- text: Pick Google and complete the sign-in.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: List the account’s calendars the person can at least read, leave out those already added, and
    save each Calendar the person picks.
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
  - entity: google-login
    effect: reads
    facts:
    - App
    - Authorization
    - Issue
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
---

# Connect Google calendars

## Trigger

The person picks Google Calendar in guided setup and is signed in.

## Outcome

The chosen calendars are saved as enabled in their Google colors, a name already in use gets a number, and setup syncs before it ends.
