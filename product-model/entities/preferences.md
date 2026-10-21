---
references:
- kind: code
  role: implementation
  target: Panel.qml#persistSettings
- kind: code
  role: implementation
  target: BarWidget.qml#cycleFormat
- kind: code
  role: implementation
  target: Model.js#normalizedWeekStart
singleton: true
---

# Preferences

The desktop’s calendar and clock preferences.

## Information kept

- **Hour cycle** — 12-hour or 24-hour display, initially inferred from the clock format with a 24-hour fallback.
- **Clock format** — The chosen date and time label format for the bar orientation.
- **Sync interval** — 5, 15, 30 or 60 minutes, or Manual; 15 minutes by default.
- **Notifications** — Whether upcoming alerts run; enabled by default.
- **Reminder timing** — Staged reminders at 10, 5 and 1 minute or one interval of 5, 10, 15 or 30 minutes; staged by default.
- **Meeting join** — Whether the direct join action is shown; enabled by default.
- **Week start** — The chosen first weekday, falling back to the system locale; controls offer Monday or Sunday.
