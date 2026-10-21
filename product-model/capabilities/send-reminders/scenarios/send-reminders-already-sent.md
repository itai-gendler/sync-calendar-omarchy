---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: A later check reaches a stage already sent.
  kind: condition
  entities: []
  unattended: true
  contexts:
    desktop:
      place: desktop::calendar
- text: Read the Event start and skip the stage.
  kind: product
  entities:
  - entity: event
    effect: reads
    facts:
    - Start
    - All day
  contexts:
    desktop:
      place: desktop::calendar
---

# Skip a reminder already sent

## Trigger

A later check finds the same event in the same reminder stage.

## Outcome

The stage is not sent again, even when a multi-day event is listed on several days.
