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
- text: Replace the form fields on the same Event at the JMAP server, clearing a location the person emptied.
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

# Edit a JMAP event

## Trigger

The person saves changes to a JMAP event.

## Outcome

The event keeps its calendar; a sync is requested and the form closes.
