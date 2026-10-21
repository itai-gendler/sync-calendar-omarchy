---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Review the title, date, times or All day, location, description and target, and save.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: Save the Event in the local Calendar on this machine, with no account or network.
  kind: product
  entities:
  - entity: calendar
    effect: reads
    facts:
    - Source
    - Connection
    - Write support
  - entity: event
    effect: creates
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
      place: desktop::event-editor
---

# Create a local event

## Trigger

The person saves a new event to the local calendar.

## Outcome

The event is saved on this machine, a sync is requested and the form closes.
