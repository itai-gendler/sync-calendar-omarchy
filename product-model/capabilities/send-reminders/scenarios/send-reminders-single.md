---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: A reminder check runs while reminders are on with one interval.
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
- text: Read the Event start and send a reminder for the chosen interval.
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

# Remind once before an event

## Trigger

Reminders are set to one interval, and a check finds a timed event starting within it.

## Outcome

One desktop notification says only when an event starts, without its title, place or calendar. All-day events get no reminder.
