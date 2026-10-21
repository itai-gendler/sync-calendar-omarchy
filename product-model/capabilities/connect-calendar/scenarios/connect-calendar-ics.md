---
kind: alternative
routes:
  guided-setup: Guided setup
steps:
- text: Pick Any .ics link and enter the link and a name.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: Fetch and read the link once, then save the Calendar.
  kind: product
  entities:
  - entity: calendar
    effect: creates
    facts:
    - Name
    - Source
    - Connection
    - Enabled
    - Color
    - Translation
    - Write support
    - Sync status
    - Event count
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
---

# Connect an iCalendar link

## Trigger

The person picks Any .ics link in guided setup.

## Outcome

The link is fetched once to check it, then saved as an enabled read-only calendar.
