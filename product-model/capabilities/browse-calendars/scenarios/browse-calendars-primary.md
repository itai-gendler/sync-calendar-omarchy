---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Open the list of configured sources.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
- text: List each Calendar with its name, source, color and whether it is enabled, and any Google login
    issue.
  kind: product
  entities:
  - entity: calendar
    effect: reads
    facts:
    - Name
    - Source
    - Enabled
    - Color
  - entity: google-login
    effect: reads
    facts:
    - Issue
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendars
---

# Review the configured calendars

## Trigger

The person opens the Calendars tab of Calendar Settings.

## Outcome

Every configured calendar is listed with its name, source, color and whether it is enabled, and a Google login problem is shown on the calendars it affects.
