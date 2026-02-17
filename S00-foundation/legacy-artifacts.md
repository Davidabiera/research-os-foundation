# Legacy Artifacts

- **Status:** reviewed
- **Owner:** operations-agent
- **Last Updated:** 2026-02-17

## Purpose
Record non-canonical legacy paths retained for compatibility. These paths are deprecated for new `initialize_project` runs.

## Legacy Paths (Read-Only)
- `docs/prd.md`
- `docs/project-plan.md`
- `artifacts/run-ledger.md`
- `task.md` (root)

## Rules
- Do not write new outputs to legacy paths.
- Do not use legacy paths as acceptance criteria for new tests.
- Canonical destinations are defined in `S00-foundation/save-map.md`.

## Migration Policy
- Keep legacy files in place until test validation is complete.
- Migrate or remove legacy files only after explicit approval.
