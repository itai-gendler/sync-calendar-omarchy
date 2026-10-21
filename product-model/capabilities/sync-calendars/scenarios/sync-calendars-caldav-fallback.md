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
- text: Read the Calendar’s published link and its Event entries.
  kind: product
  entities:
  - entity: calendar
    effect: changes
    facts:
    - Sync status
    - Event count
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
---

# Read a CalDAV calendar through its published link

## Trigger

Reading a CalDAV calendar fails and the same entry also has a published iCalendar link.

## Outcome

The published link is read instead; new events and edits still go to the CalDAV calendar.
