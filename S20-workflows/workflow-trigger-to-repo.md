# Workflow: Trigger to Repo

- **Status:** reviewed
- **Owner:** builder-agent
- **Last Updated:** 2026-02-16

## Goal
Turn an initial trigger (idea/request) into a ready-to-run project repository with a standard startup artifact set.

## Contract Binding
When this workflow is executed through `initialize_project`, `S20-workflows/initialize-project-contract.md` is authoritative for inputs, output paths, protections, and overwrite policy.

## Inputs
1. **PRD Text**: The current draft requirement narrative in plain text or markdown.
2. **PRD Source**: Where the PRD text came from (chat transcript, ticket, notes file, workshop doc, or linked specification).
3. **Project Metadata**: Project name, owner, objective, timeline, and delivery constraints.

## Process
1. **Create PRD**
   * Create `S00-foundation/prd.md` from `S20-workflows/templates/prd-template.md`.
   * Record PRD source references in the PRD (links, filenames, and/or transcript IDs).
2. **Create Project Folder**
   * Create a new top-level project directory using kebab-case.
   * Ensure startup folders include `S00-foundation/`, `S20-workflows/`, `src/`, and `tests/` unless a domain-specific structure is already defined.
3. **Create Initial Artifacts**
   * Save `S00-foundation/prd.md`.
   * Save `S20-workflows/project-plan.md` with phases, milestones, and first implementation tasks.
   * Save `S20-workflows/run-ledger.md` initialized from `S20-workflows/run-ledger-schema.md`.
   * Save `S20-workflows/task.md` for first-run task checklist.
   * Save `S00-foundation/context.md` using the PRD source content.
   * Save project `README.md` with purpose, setup, and operating loop reference.
4. **Initialize Repo**
   * Initialize Git if missing.
   * Create `.gitignore` appropriate for stack/tooling.
   * Make the initial commit with the startup artifact set.
5. **Open in Codex**
   * Open the project root in Codex.
   * Confirm `AGENTS.md` (or equivalent agent entrypoint) exists.
   * Start the first execution cycle using `workflow-context-to-output.md`.

## Outputs
A consistent startup file set is created:
- `README.md`
- `S00-foundation/prd.md`
- `S00-foundation/context.md`
- `S20-workflows/project-plan.md`
- `S20-workflows/run-ledger.md`
- `S20-workflows/task.md`
- `.gitignore`
- `src/`
- `tests/`

Also produced:
- Initial commit capturing startup artifacts.
- Codex-ready workspace with a clear first-run path.

## Quality Gate
- [ ] PRD includes measurable success criteria and source traceability.
- [ ] Folder and file names follow living file naming conventions.
- [ ] Run ledger is initialized before first implementation run.
- [ ] Repository is committed and can be cloned and run by another contributor.
