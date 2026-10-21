---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: Choose Delete, then confirm while it is armed.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Ask the JMAP server to delete the Event it returned; what that means for a recurring series is
    the server’s decision.
  kind: product
  entities:
  - entity: event
    effect: removes
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Delete a JMAP event

## Trigger

The person deletes an event from a JMAP account.

## Outcome

After the second click within four seconds, the JMAP server deletes the event, and the next sync updates the agenda.
