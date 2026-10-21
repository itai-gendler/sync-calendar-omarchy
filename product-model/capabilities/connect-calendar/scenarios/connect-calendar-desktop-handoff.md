---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Choose guided connection.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
- text: Open guided setup in a terminal.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: setup
- text: Pick a provider, enter what it asks for and pick any sources offered.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: setup
- text: Check or discover the source, save each Calendar and sync.
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
    desktop:
      place: setup
---

# Connect from Calendar Settings

## Trigger

The person chooses Connect a calendar in Calendar Settings.

## Outcome

Guided setup runs in a terminal; when it ends, the panel reloads its calendars and syncs.
