---
kind: alternative
routes:
  guided-setup: Guided setup
steps:
- text: Pick Fastmail / JMAP and enter the session URL, API token and a name.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: Check the token with a test fetch, then save the Calendar.
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

# Connect a JMAP account

## Trigger

The person picks Fastmail / JMAP in guided setup.

## Outcome

The token is checked by fetching events, then the account is saved as one enabled calendar.
