---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: Turn on All day and save.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: Save the Event as all-day on its date, dropping its times.
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

# Change an event to all-day

## Trigger

The person turns on All day while editing a timed event.

## Outcome

The event keeps its calendar and now occupies its date without times; a sync is requested and the form closes.
