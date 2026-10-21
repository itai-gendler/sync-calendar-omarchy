---
kind: primary
result: achieved
routes:
  shell-commands: Shell commands
steps:
- text: Ask for the creation form from a shell command, with a sentence.
  kind: actor
  entities: []
  capability: prepare-event
  actor: desktop-user
  contexts:
    shell-commands:
      place: shell-commands
- text: Open the creation form, filled from the sentence.
  kind: product
  entities: []
  capability: prepare-event
  actor: desktop-user
  contexts:
    shell-commands:
      place: desktop::event-editor
- text: Review the values and save.
  kind: actor
  entities: []
  capability: create-event
  actor: desktop-user
  contexts:
    shell-commands:
      place: desktop::event-editor
- text: Create the Event in the chosen Calendar.
  kind: product
  entities:
  - entity: calendar
    effect: reads
    facts:
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
  capability: create-event
  actor: desktop-user
  contexts:
    shell-commands:
      place: desktop::event-editor
---

# Save an event prepared by a shell command

## Trigger

A key binding asks Chronica for the event form with a Quick Add sentence.

## Outcome

The reviewed event is saved in the chosen calendar.
