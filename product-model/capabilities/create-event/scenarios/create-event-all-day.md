---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: Enter a title and date, turn on All day and save.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: Create the Event on that date in the chosen Calendar.
  kind: product
  entities:
  - entity: calendar
    effect: reads
    facts:
    - Source
    - Connection
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

# Create an all-day event

## Trigger

The person turns on All day in the event form.

## Outcome

The event occupies its one date. Google and CalDAV receive an exclusive end date; JMAP receives a one-day duration.
