---
kind: alternative
routes:
  guided-setup: Guided setup
steps:
- text: Pick iCloud or CalDAV, and enter the server, account and app password.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: Discover the account’s calendars, leave out those already added, and save each Calendar the person
    picks.
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
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
---

# Connect CalDAV or iCloud calendars

## Trigger

The person picks Apple iCloud or Nextcloud / CalDAV in guided setup.

## Outcome

The chosen calendars are saved as enabled, a name already in use gets a number, and setup syncs before it ends.
