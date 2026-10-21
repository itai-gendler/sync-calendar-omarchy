---
kind: primary
routes:
  desktop: Desktop
steps:
- text: A reminder check runs while staged reminders are on.
  kind: condition
  entities:
  - entity: preferences
    effect: reads
    facts:
    - Notifications
    - Reminder timing
  unattended: true
  contexts:
    desktop:
      place: desktop::calendar
- text: Read the Event start and send a reminder for the current 10-, 5- or 1-minute stage.
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

# Remind at 10, 5 and 1 minutes

## Trigger

Reminders are staged, and a check finds a timed event starting within 10 minutes.

## Outcome

A desktop notification for the current stage says only when an event starts, without its title, place or calendar. All-day events get no reminder.
