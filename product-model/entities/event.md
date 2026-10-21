---
domain: agenda
references:
- kind: code
  role: implementation
  target: fetch-events.py#parse_ics
- kind: code
  role: implementation
  target: fetch-events.py#sync_all_events
- kind: code
  role: implementation
  target: Panel.qml#submitEvent
---

# Event

An event from a calendar, shown on each date it covers. An occurrence of a recurring event keeps the identity its provider needs to change or delete it.

## Information kept

- **Title** — The event’s title.
- **Start** — Its start date and local display time.
- **End** — Its end date and local display time.
- **All day** — Whether it occupies dates without a clock time.
- **Location** — Its supplied place or meeting text.
- **Description** — Its supplied details.
- **Calendar** — The calendar it comes from, kept on edits.
- **Recurrence** — The source recurrence and exception information needed to present occurrences.
- **Meeting link** — A detected supported meeting address and provider label, or no link.
- **Writable** — Whether the panel offers Delete for it.
- **Editable** — Whether the one-day form can edit it.
