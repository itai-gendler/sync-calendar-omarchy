---
kind: primary
routes:
  desktop: Desktop
steps:
- text: A sync reads a Calendar with translation on.
  kind: condition
  entities:
  - entity: calendar
    effect: reads
    facts:
    - Translation
  unattended: true
  contexts:
    desktop:
      place: desktop::calendar
- text: Translate Korean Event titles and locations through Google Translate.
  kind: product
  entities:
  - entity: event
    effect: changes
    facts:
    - Title
    - Location
  contexts:
    desktop:
      place: desktop::calendar
---

# Translate a calendar’s Korean events

## Trigger

A sync reads a calendar with translation turned on.

## Outcome

Korean titles and locations show in English when translation succeeds; earlier translations are reused.
