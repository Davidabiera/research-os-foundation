# Save Map

- **Status:** reviewed
- **Owner:** operations-agent
- **Last Updated:** 2026-02-17

## Purpose
Provide a deterministic routing table for where `initialize_project` writes each startup artifact.

## Canonical Routes
| Artifact Type | Canonical Path | Write Policy |
|---|---|---|
| PRD | `S00-foundation/prd.md` | Create if missing; version up if changed |
| Project Plan | `S20-workflows/project-plan.md` | Create if missing; version up if changed |
| Run Ledger | `S20-workflows/run-ledger.md` | Append-only |
| Context | `S00-foundation/context.md` | Create if missing; version up if changed |
| Task List | `S20-workflows/task.md` | Append/update checklist; preserve history |
| README Summary | `README.md` between summary markers | Update block only |

## Compatibility Notes
- Legacy paths like `docs/prd.md` and `artifacts/run-ledger.md` may exist from earlier runs.
- New `initialize_project` runs should prioritize canonical routes in this file.
- Do not duplicate the same artifact in multiple active locations unless explicitly requested.
- See `S00-foundation/legacy-artifacts.md` for explicit deprecated paths and handling rules.
