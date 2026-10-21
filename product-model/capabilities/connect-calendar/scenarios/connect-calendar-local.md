---
kind: alternative
routes:
  guided-setup: Guided setup
steps:
- text: Pick the local option and enter a name.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: Save a local offline Calendar.
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

# Add a local calendar in guided setup

## Trigger

The person picks Local calendar in guided setup.

## Outcome

A local offline calendar is saved without contacting any provider.
