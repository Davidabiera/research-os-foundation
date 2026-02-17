---
name: initialize_project
description: "Initialize a project workspace using a strict contract, save-map routing, and deterministic run reporting."
---

# Initialize Project

## Purpose
Transform a foundation repo into a project workspace using one canonical contract and explicit artifact routing.

## Canonical References
- `S20-workflows/initialize-project-contract.md` (single source of truth)
- `S00-foundation/save-map.md` (artifact routing table)

## Required Inputs
- `project_name`
- `goal`
- `owner`
- `constraints`
- `source`

If any required input is missing, stop before edits and return Run Report with warnings.

## Required Outputs
- `S00-foundation/prd.md`
- `S00-foundation/context.md`
- `S20-workflows/project-plan.md`
- `S20-workflows/run-ledger.md`
- `S20-workflows/task.md`
- `README.md` (summary block only)
- `.gitignore`
- `src/`
- `tests/`

## Steps
1. Validate required inputs using contract rules.
2. Resolve destination paths through `S00-foundation/save-map.md`.
3. Create or update startup artifacts per overwrite policy:
   - Create-if-missing for required outputs.
   - Append-only for run ledger.
   - Append/update checklist behavior for task list.
   - Version-up for material changes to PRD/context/project plan.
4. Update README summary text only between:
   - `<!-- PROJECT_SUMMARY_START -->`
   - `<!-- PROJECT_SUMMARY_END -->`
5. Apply do-not-touch protections from the contract.
6. Emit Run Report in the required format.

## Stop Rules
- Never edit protected paths defined in `S20-workflows/initialize-project-contract.md`.
- Never edit README content outside summary markers.
- Never rewrite run ledger history.

## Required Run Report Format
At end of every run, output:

1. **Created:** semicolon-separated created paths.
2. **Updated:** semicolon-separated updated paths.
3. **Skipped:** protected or intentionally unchanged paths.
4. **Warnings:** missing inputs, overwrite prevention events, policy conflicts.
5. **Next suggested action:** first executable follow-up task.
