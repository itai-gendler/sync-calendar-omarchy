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
- text: Delete the Event at Google; for a recurring event, only the chosen occurrence.
  kind: product
  entities:
  - entity: event
    effect: removes
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Delete a Google event or one occurrence

## Trigger

The person deletes an event from a Google calendar.

## Outcome

After the second click within four seconds, Google deletes that event, or only that occurrence of a recurring one, and the next sync updates the agenda.
