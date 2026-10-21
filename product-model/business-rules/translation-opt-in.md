---
appliesTo:
- type: entity
  id: event
  effect: changes
  facts:
  - Title
  - Location
  contexts:
  - place: desktop::calendar
references:
- kind: code
  role: implementation
  target: fetch-events.py#translate_korean_to_english
- kind: code
  role: implementation
  target: fetch-events.py#parse_ics
permits:
- unattended: true
  when:
  - entity: calendar
    fact: Translation
    is: true
---

# Automatic translation changes only text from calendars that turn it on

A calendar’s translation option lets Korean titles and locations be translated into English for display. The translation is never written back to the provider.
