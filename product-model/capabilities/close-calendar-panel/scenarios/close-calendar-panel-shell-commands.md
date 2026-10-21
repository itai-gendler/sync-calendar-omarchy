---
kind: primary
routes:
  shell-commands: Shell commands
steps:
- text: Ask to close the panel from a shell command.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    shell-commands:
      place: shell-commands
- text: Close the panel, discarding any unsaved input.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    shell-commands:
      place: shell-commands
---

# Close the panel from a shell command

## Trigger

A key binding or script asks Chronica to close the panel.

## Outcome

The panel closes, and any unsaved event, settings or life progress input is discarded.
