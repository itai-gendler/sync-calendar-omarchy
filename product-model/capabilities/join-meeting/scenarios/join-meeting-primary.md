---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Choose Join.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Open the Event meeting link with the desktop’s handler and close the panel.
  kind: product
  entities:
  - entity: event
    effect: reads
    facts:
    - Meeting link
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Join a meeting

## Trigger

The person chooses Join on an event with a detected meeting link.

## Outcome

The meeting opens in the desktop’s browser or app and the panel closes; the meeting service handles admission.
