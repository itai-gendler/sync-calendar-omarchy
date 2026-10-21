---
id: chronica
summary: Calendar and clock for the Omarchy desktop, with calendar synchronization, event editing and
  reminders.
category: productivity
tags:
- calendar
- desktop
- scheduling
authors:
- name: promaaa
license: MIT
languages:
- en
limitations:
- Remote calendars remain hosted by their providers; Chronica uses their feeds and APIs and their access
  decisions.
- The event form creates and edits single-day events; recurrence schedules and multi-day spans are read
  from existing calendars.
- Published iCalendar subscriptions are read-only.
- Local offline events stay on this machine; remote writes require the provider to accept the change.
- iCalendar recurrence expansion supports daily, weekly, monthly and yearly schedules.
references:
- kind: doc
  role: intent
  target: README.md
- kind: code
  role: implementation
  target: manifest.json
- kind: code
  role: implementation
  target: Panel.qml
- kind: code
  role: implementation
  target: fetch-events.py
---

# Chronica

Chronica puts calendars and a clock in the Omarchy desktop bar. People browse a month and agenda, create, edit and delete supported events, join meetings, copy their agenda and receive reminders. It supports the stock Omarchy bar and Shibumi Shell, Google Calendar, CalDAV, JMAP, published iCalendar feeds and a local offline calendar.

## Intent

“Every calendar you own, in your Omarchy bar.” The project promises two-way event work “without leaving the desktop,” plus reminders, one-click meeting join and an offline calendar when no account is available. The desktop panel is the everyday workspace; guided setup connects accounts through each provider’s own authorization and discovery process.
