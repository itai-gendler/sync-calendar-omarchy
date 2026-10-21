---
kind: primary
routes:
  desktop: Desktop
steps:
- text: Read the sign-in banner.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
- text: Name the affected Calendar sources and the Google login issue, telling a missing login from an
    expired one.
  kind: product
  entities:
  - entity: calendar
    effect: reads
    facts:
    - Name
    - Sync status
  - entity: google-login
    effect: reads
    facts:
    - Issue
  actor: desktop-user
  contexts:
    desktop:
      place: desktop::calendar
---

# See a Google login problem

## Trigger

A Google calendar’s sync reports a missing or rejected login.

## Outcome

A banner names the affected calendars, says whether the login is missing or expired, and offers to reconnect.
