---
kind: primary
result: achieved
routes:
  desktop: From the clock
  command: From a shell command
steps:
- text: Open the panel.
  capability: open-calendar-panel
  kind: actor
  actor: desktop-user
  entities: []
  contexts:
    desktop:
      place: desktop::clock
    command:
      place: shell-commands
- text: Show the panel at today.
  capability: open-calendar-panel
  kind: product
  actor: desktop-user
  entities: []
  contexts:
    desktop:
      place: desktop::calendar
    command:
      place: desktop::calendar
- text: Read today’s Event entries.
  capability: browse-agenda
  kind: actor
  actor: desktop-user
  entities:
  - entity: event
    effect: reads
    facts:
    - Title
    - Start
    - End
    - All day
    - Calendar
  contexts:
    desktop:
      place: desktop::calendar
    command:
      place: desktop::calendar
---

# Reach today’s agenda

## Trigger

The person opens the panel from the clock or a shell command.

## Outcome

Today’s agenda is shown, or an empty day.
