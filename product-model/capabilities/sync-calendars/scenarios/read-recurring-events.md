---
kind: alternative
routes:
  desktop: Desktop
steps:
- text: Request a sync.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Expand each recurring Event in its source time zone and convert the occurrences to the desktop
    time zone.
  kind: product
  entities:
  - entity: event
    effect: reads
    facts:
    - Title
    - Start
    - End
    - All day
    - Location
    - Description
    - Calendar
    - Recurrence
    - Meeting link
    - Writable
    - Editable
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Record the Calendar sync result.
  kind: product
  entities:
  - entity: calendar
    effect: changes
    facts:
    - Sync status
    - Event count
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# Read recurring events across clock changes

## Trigger

A calendar holds daily, weekly, monthly or yearly recurring events, with exceptions.

## Outcome

Occurrences show in local time at their source wall-clock time, honoring interval, count, until, extra dates and exclusions; Google and JMAP can supply occurrences already expanded.
