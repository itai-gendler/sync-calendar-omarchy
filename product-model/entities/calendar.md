---
domain: calendars
references:
- kind: code
  role: implementation
  target: fetch-events.py#calendar_kind
- kind: code
  role: implementation
  target: fetch-events.py#sync_all_events
- kind: code
  role: implementation
  target: Model.js#getWritableCalendars
- kind: code
  role: implementation
  target: Panel.qml#commitNewCalendar
relations:
- entity: event
  verb: supplies
  cardinality: one-to-many
---

# Calendar

A calendar Chronica shows: a Google, CalDAV or JMAP calendar, an iCalendar link, or the local offline calendar.

## Information kept

- **Name** — The name used to choose and identify this source.
- **Source** — Local offline, Google API, CalDAV, JMAP or iCalendar subscription.
- **Connection** — The source address or calendar selection and the authorization material needed by that source; local offline has no remote connection.
- **Enabled** — Whether this configured source participates in synchronization.
- **Color** — The chosen source color used to identify its events.
- **Translation** — Whether Korean titles and locations are translated to English; off by default.
- **Write support** — Whether this source has a supported event-writing connection; the external provider still decides whether a request succeeds.
- **Sync status** — The latest source fetch result, including a Google login issue where relevant.
- **Event count** — The number of expanded event entries returned by the latest fetch.
