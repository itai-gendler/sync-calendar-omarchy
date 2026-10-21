---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: Type a Quick Add sentence in the title field and apply it.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: Fill the title Lunch, tomorrow’s date and 13:00–14:00, keeping words it does not recognize in
    the title.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: Review the filled fields and save.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: Create the Event in the chosen Calendar and request a sync.
  kind: product
  entities:
  - entity: calendar
    effect: reads
    facts:
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

# Fill the form from a Quick Add sentence

## Trigger

The person types Lunch tomorrow 1pm-2pm in the title field and applies Quick Add.

## Outcome

The form holds Lunch, tomorrow’s date and 13:00–14:00, and the event is saved only when the person saves it.
