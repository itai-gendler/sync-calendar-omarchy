---
kind: validation
routes:
  desktop: Desktop
steps:
- text: Leave the name, or the link, ID or JMAP token, empty and confirm.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
- text: Keep the add form open without saving.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
---

# Leave a required field empty

## Trigger

The person adds a calendar by hand without a name, or without the link, calendar ID or token its type needs.

## Outcome

Nothing is saved and the form stays open for the missing value.
