---
kind: primary
routes:
  shell-commands: Shell commands
steps:
- text: Ask for the creation form from a shell command, optionally with a sentence.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    shell-commands:
      place: shell-commands
- text: Open the creation form for today, filled from the sentence when there is one.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    shell-commands:
      place: desktop::event-editor
---

# Prepare an event from a shell command

## Trigger

A key binding or script asks Chronica for the event form, optionally with a Quick Add sentence.

## Outcome

The panel opens on the event form for today, or for the date and times read from the sentence; nothing is saved until the person saves it.
