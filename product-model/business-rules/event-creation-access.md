---
appliesTo:
- type: entity
  id: event
  effect: creates
references:
- kind: code
  role: implementation
  target: Model.js#getWritableCalendars
- kind: code
  role: implementation
  target: fetch-events.py#create_event
- kind: code
  role: implementation
  target: fetch-events.py#google_request
permits:
- actors:
  - desktop-user
  when:
  - entity: calendar
    fact: Write support
    is: true
  - entity: calendar
    fact: Enabled
    is: true
---

# Only the desktop user creates events, in calendars Chronica can write to

Creating is offered for enabled local, Google, JMAP and CalDAV calendars; a CalDAV calendar needs its account and password. An iCalendar link has nothing to write to. The provider still decides whether it accepts the event.

For Google, a sign-in without write access gets a reconnect instruction. Other refusals keep the provider’s explanation; a calendar the account can only read is not fixed by signing in again.
