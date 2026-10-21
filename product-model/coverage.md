---
scope: The desktop calendar and clock, guided account setup, supported shell commands, event writes, synchronization
  and reminders.
method: Static inspection of tracked implementation and product documentation at 5f0251c97cd5104a172e606b0c51977915517300.
covered:
- description: Desktop clock and panel workflow code, including account connections, event forms,
    preferences, agenda and personal progress.
  paths:
  - BarWidget.qml
  - Panel.qml
  - Model.js
- description: Provider integration, event parsing, writes, synchronization, reminder dispatch and explicit
    cleanup code.
  paths:
  - fetch-events.py
  - Backend.qml
- description: Guided connection and Google authorization flow code.
  paths:
  - setup.py
  - google-auth.py
exclusions:
- description: Presentation primitives and screenshot assets are design, not product behavior.
  paths:
  - BoundedTextField.qml
  - ChoicePill.qml
  - add-event.webp
  - full-preview.webp
  - settings.webp
  - preview.png
- description: CI and test infrastructure are development support rather than product interaction contracts.
  paths:
  - .github/
  - tests/
- description: Static setup-guide styling and project metadata provide authoring context, not a separately
    mapped web product.
  paths:
  - docs/
  - manifest.json
  - LICENSE
  - .gitignore
  - README.md
unmapped:
- description: Backend diagnostic flags and raw helper request protocol are implementation support without
    a separately established user API contract.
  paths:
  - fetch-events.py
- description: Advanced hand-edited source configuration beyond the guided and panel workflows remains
    documented context rather than a separate file-editing interface.
  paths:
  - fetch-events.py
  - README.md
- description: Upcoming-view Markdown export formatting is outside the mapped selected-day export scope.
  paths:
  - Panel.qml
  - Model.js
- description: Interactions among multiple configured local source entries are outside the mapped single-local-source
    workflow.
  paths:
  - fetch-events.py
  - Model.js
limitations: []
---

# Coverage


