---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Select an Event in the agenda.
  kind: actor
  entities:
  - entity: event
    effect: reads
    facts:
    - Title
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Open the Event details, or say there is no description.
  kind: product
  entities:
  - entity: event
    effect: reads
    facts:
    - Title
    - Start
    - End
    - All day
    - Location
    - Description
    - Calendar
    - Recurrence
    - Meeting link
    - Writable
    - Editable
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Read an event’s details

## Trigger

The person selects an event in the agenda.

## Outcome

The event opens to show its full title and its description, or a note that it has none.
