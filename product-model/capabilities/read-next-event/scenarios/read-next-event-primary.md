---
kind: primary
routes:
  shell-commands: Shell commands
steps:
- text: Ask what comes next from a shell command.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    shell-commands:
      place: shell-commands
- text: Return the Event time range and title, or nothing.
  kind: product
  entities:
  - entity: event
    effect: reads
    facts:
    - Title
    - Start
    - End
    - All day
  - entity: preferences
    effect: reads
    facts:
    - Hour cycle
  actor: desktop-user
  contexts:
    shell-commands:
      place: shell-commands
---

# Read the next event from a shell command

## Trigger

A key binding or script asks Chronica for the next event.

## Outcome

It returns the time range and title of the next timed event that has not started yet, today or tomorrow, or nothing.
