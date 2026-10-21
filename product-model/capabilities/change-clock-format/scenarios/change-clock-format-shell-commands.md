---
kind: primary
routes:
  shell-commands: Shell commands
steps:
- text: Ask for the next clock format from a shell command.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    shell-commands:
      place: shell-commands
- text: Change Preferences to the next distinct format and its hour cycle.
  kind: product
  entities:
  - entity: preferences
    effect: changes
    facts:
    - Clock format
    - Hour cycle
  actor: desktop-user
  contexts:
    shell-commands:
      place: shell-commands
---

# Cycle the clock format from a shell command

## Trigger

A key binding or script asks Chronica for the next clock format.

## Outcome

The clock shows the next format at once, with its hour cycle, and keeps it from then on when the bar can save its settings.
