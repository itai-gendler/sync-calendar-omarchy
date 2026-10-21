---
kind: alternative
routes:
  guided-setup: Guided setup
steps:
- text: Interrupt setup before anything is saved.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: End setup without adding a source, keeping any Google login already saved.
  kind: product
  entities:
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

# Cancel guided setup

## Trigger

The person interrupts guided setup before any calendar is saved.

## Outcome

No calendar is added; a Google sign-in completed before cancelling stays saved.
