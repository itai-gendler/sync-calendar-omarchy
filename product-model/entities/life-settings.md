---
domain: memento-mori
references:
- kind: code
  role: implementation
  target: Panel.qml#commitLife
- kind: code
  role: implementation
  target: Model.js#parseBirthYear
- kind: code
  role: implementation
  target: Model.js#parseLifeExpectancy
singleton: true
---

# Life settings

The personal values used by Memento Mori.

## Information kept

- **Birth year** — A four-digit year no more than 120 years before the current year; unset hides life progress.
- **Life expectancy** — The chosen lifespan in years, from 1 through 150, with a default of 90.
