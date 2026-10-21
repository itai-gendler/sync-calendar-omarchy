---
kind: alternative
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
- text: Create the Event in the chosen CalDAV Calendar.
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

# Create a CalDAV event

## Trigger

The person saves a new event to a CalDAV or iCloud calendar.

## Outcome

The event is saved at the provider, a sync is requested and the form closes.
