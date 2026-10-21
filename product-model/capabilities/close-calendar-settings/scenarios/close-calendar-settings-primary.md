---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Go back to the month and agenda.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::preferences
- text: Close the settings and show the month and agenda again, dropping an unsaved add form.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Go back to the calendar

## Trigger

The person goes back from Calendar Settings to the calendar.

## Outcome

The month and agenda are shown again; a calendar being added by hand and not yet saved is discarded.
