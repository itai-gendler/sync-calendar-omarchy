---
kind: primary
routes:
  desktop: Desktop
steps:
- text: A sync needs Google access and the saved access has expired.
  kind: condition
  entities: []
  unattended: true
  contexts:
    desktop:
      place: desktop::calendar
- text: Renew the Google login access and keep it connected.
  kind: product
  entities:
  - entity: google-login
    effect: changes
    from: Connected
    to: Connected
    facts:
    - Authorization
    - Issue
  contexts:
    desktop:
      place: desktop::calendar
---

# Renew Google access

## Trigger

A sync needs Google access and the saved access has expired.

## Outcome

Fresh access is saved and any earlier login problem is cleared.
