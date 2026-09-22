# Crank

- **Dates:** 2026 → present
- **Status:** Active
- **Stack:** Python, Claude Code, GLM, YAML pipelines

A pipeline runner for coding agents where the gates decide, not the model.

Every task walks through requirements written in EARS, design, tasks, implementation, validation, a "metahuman" phase and documentation. Each phase ends in an adversarial review by a read-only reviewer: a finding of medium severity or above sends the phase back, with the review as feedback. Fidelity validators check the requirements against the existing code, the design against the requirements and the implementation against the spec, and the real test suite acts as a mechanical gate.

## Metahuman

The phase after every quality gate, test and coverage threshold. An agent tries the feature the way a QA engineer would: it opens Chrome and uses it, reads screenshots, calls the API and looks for edge cases. It cannot touch the code, and the severity of each finding decides where the task goes back to.

## Details

- Pipelines and model backends are declared in YAML, with Claude Code and GLM as backends.
- A web panel follows several projects at once.
- 94% test coverage.
