---
kind: edge
routes:
  guided-setup: Guided setup
steps:
- text: Start the Google sign-in.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: Report the unfinished sign-in and stop waiting.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
---

# End an unfinished Google sign-in

## Trigger

Consent is cancelled, ten minutes pass without an answer, or Google’s code cannot be exchanged.

## Outcome

Setup reports that the sign-in failed, and no new login is saved.
