---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Copy the day’s agenda.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Copy each Event’s time, title and meeting link or location to the clipboard as Markdown tasks,
    and confirm the copy.
  kind: product
  entities:
  - entity: event
    effect: reads
    facts:
    - Title
    - Start
    - End
    - All day
    - Meeting link
    - Location
  - entity: preferences
    effect: reads
    facts:
    - Hour cycle
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Copy the day’s agenda as Markdown

## Trigger

The person copies the selected day’s agenda.

## Outcome

The clipboard holds a Markdown task list headed by the date and any calendar filter, one line per event with its time, title and meeting link or location; the panel confirms the copy.
