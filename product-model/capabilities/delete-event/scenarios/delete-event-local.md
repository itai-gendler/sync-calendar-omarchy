---
kind: primary
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
- text: Delete the Event from the local offline store.
  kind: product
  entities:
  - entity: event
    effect: removes
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Delete a local event

## Trigger

The person deletes an event from the local calendar.

## Outcome

After the second click within four seconds, the event is deleted from this machine, and the next sync updates the agenda.
