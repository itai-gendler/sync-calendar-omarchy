---
kind: validation
routes:
  desktop: Desktop
steps:
- text: Save with an invalid field.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
- text: Keep the form open with a message naming what to correct.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::event-editor
---

# Correct invalid event input

## Trigger

The person saves with an empty title, a date that is not a real date, a time that cannot be read, or an end time at or before the start.

## Outcome

Nothing is saved; the form keeps the input and says what to correct.
