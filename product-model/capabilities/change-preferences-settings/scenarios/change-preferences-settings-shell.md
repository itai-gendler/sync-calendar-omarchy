---
kind: alternative
routes:
  shell-commands: Shell commands
steps:
- text: Ask to toggle the first weekday from a shell command.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    shell-commands:
      place: shell-commands
- text: Change the Preferences week start.
  kind: product
  entities:
  - entity: preferences
    effect: changes
    facts:
    - Week start
  actor: desktop-user
  contexts:
    shell-commands:
      place: shell-commands
---

# Toggle the first weekday from a shell command

## Trigger

A key binding or script asks Chronica to toggle the first weekday.

## Outcome

A Monday start becomes Sunday and any other start becomes Monday; the month grid follows at once.
