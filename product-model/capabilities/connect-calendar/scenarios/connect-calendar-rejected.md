---
kind: edge
routes:
  guided-setup: Guided setup
steps:
- text: Enter the connection details.
  kind: actor
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
- text: Report the failed check without adding a source.
  kind: product
  entities: []
  actor: desktop-user
  contexts:
    guided-setup:
      place: setup
---

# Stop when a connection check fails

## Trigger

The JMAP token or iCalendar link fails its check, or CalDAV discovery or the Google calendar list fails.

## Outcome

Setup reports the error and points to the setup guide; no calendar is added.
