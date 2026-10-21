---
availability:
- place: desktop
references:
- kind: code
  role: implementation
  target: Model.js#ageFromBirthYear
- kind: code
  role: implementation
  target: Model.js#lifeProgressPercent
domain: memento-mori
---

# Read life progress

Read Memento Mori progress when a valid birth year has been set. Age is the current year minus birth year, without birthday precision.
