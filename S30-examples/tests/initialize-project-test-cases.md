# Initialize Project Test Cases

- **Status:** reviewed
- **Owner:** qa-agent
- **Last Updated:** 2026-02-17

## Usage
Run `initialize_project` once per test case in an isolated copy of the foundation repo. Compare resulting files against expected outputs below.

## Test Case 1: Minimal PRD (Internal Tool)
### Input Metadata
- `project_name`: `internal-notes-assistant`
- `goal`: `Create a searchable internal notes assistant for weekly operations updates.`
- `owner`: `ops-team`
- `constraints`: `2-week timeline; markdown-only outputs; no external integrations in v1.`
- `source`: `manual intake from planning call notes`

### Expected Created Files
- `S00-foundation/prd.md`
- `S00-foundation/context.md`
- `S20-workflows/project-plan.md`
- `S20-workflows/run-ledger.md`
- `S20-workflows/task.md`
- `.gitignore`
- `src/`
- `tests/`

### Expected README Change
- Only text inside `<!-- PROJECT_SUMMARY_START -->` and `<!-- PROJECT_SUMMARY_END -->` is changed.

### Expected Ledger Entry Line
- One new row appended to `S20-workflows/run-ledger.md` with:
  - `workflow_used=initialize_project`
  - `review_status=draft`
  - `promotion_target=none`

## Test Case 2: Client-Like Project (Higher Constraints)
### Input Metadata
- `project_name`: `client-research-briefing-pipeline`
- `goal`: `Produce weekly client research briefings with standardized structure and approvals.`
- `owner`: `delivery-lead`
- `constraints`: `SOC2 handling; legal review required before publication; fixed weekly delivery window.`
- `source`: `client statement of work and kickoff transcript`

### Expected Created Files
- Same baseline output set as Test Case 1.

### Expected README Change
- Summary block references client briefing objective and constraint-aware language.

### Expected Ledger Entry Line
- One appended row includes constraints summary in notes and same workflow/review defaults.

## Test Case 3: Sensitive Mode (Strict Permissions)
### Input Metadata
- `project_name`: `sensitive-governance-audit-assistant`
- `goal`: `Support internal governance audit preparation with restricted handling rules.`
- `owner`: `compliance-team`
- `constraints`: `No writes to protected sections; append-only ledger; no external links in artifacts.`
- `source`: `internal compliance memo and audit checklist`

### Expected Created Files
- Same baseline output set as Test Case 1.

### Expected README Change
- Summary block updated, with no edits outside protected markers.

### Expected Ledger Entry Line
- One appended row with notes indicating protected-write restrictions were honored.

## Pass/Fail Checklist
- [ ] All required output paths exist.
- [ ] No edits occurred in protected sections from contract do-not-touch list.
- [ ] README edits are limited to protected summary block.
- [ ] Ledger has exactly one new appended row per run.
- [ ] Run report includes Created, Updated, Skipped, Warnings, and Next suggested action.
