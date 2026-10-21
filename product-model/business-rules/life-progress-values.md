---
appliesTo:
- type: entity
  id: life-settings
- type: capability
  id: read-life-progress
- type: capability
  id: change-life-settings
references:
- kind: code
  role: implementation
  target: Model.js#parseBirthYear
- kind: code
  role: implementation
  target: Model.js#ageFromBirthYear
- kind: code
  role: implementation
  target: Model.js#parseLifeExpectancy
- kind: code
  role: implementation
  target: Model.js#lifeProgress
---

# Life progress uses calendar-year age and the chosen expectancy

Age is current year minus birth year. A valid birth year lies within the last 120 years, including the current year. Expectancy is 1–150 years with a default of 90. Progress is clamped to 0–100 percent; an unset birth year hides it.
