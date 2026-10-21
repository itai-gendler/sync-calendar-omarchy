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
- text: Create the Event in the JMAP Calendar the entry names, or in the account’s default writable calendar
    when it names none.
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

# Create a JMAP event

## Trigger

The person saves a new event to a JMAP account.

## Outcome

The event is saved on the JMAP server, a sync is requested and the form closes.
