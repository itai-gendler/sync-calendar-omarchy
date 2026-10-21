---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: Change the form fields and save.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: Read the Event from the server, finding it by its UID if needed, replace only the form fields
    and keep its alarms, attendees and other properties.
  kind: product
  entities:
  - entity: event
    effect: changes
    facts:
    - Title
    - Start
    - End
    - All day
    - Location
    - Description
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
---

# Edit a CalDAV event

## Trigger

The person saves changes to a CalDAV or iCloud event.

## Outcome

The event keeps its calendar, alarms and attendees; a sync is requested and the form closes.
