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
- text: Change only the chosen occurrence of the Event at Google, clearing fields the person emptied.
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

# Edit one occurrence of a Google event

## Trigger

The person saves changes to one occurrence of a recurring Google event.

## Outcome

Only that occurrence changes; the rest of the series is untouched.
