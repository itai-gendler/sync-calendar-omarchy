---
kind: primary
routes:
  shell-commands: Shell commands
steps:
- text: Ask to open the panel from a shell command.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    shell-commands:
      place: shell-commands
- text: Show the panel at today, reload saved data and sync if due.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    shell-commands:
      place: desktop::calendar
---

# Open the panel from a shell command

## Trigger

A key binding or script asks Chronica to open the panel.

## Outcome

The panel shows today and reloads the saved events, and it syncs unless it synced in the last 30 seconds.
