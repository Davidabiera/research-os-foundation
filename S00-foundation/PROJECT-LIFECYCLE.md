# Project Lifecycle

Every project in this OS moves through 4 distinct stages.

## Stage 1: Idea (Trigger)
*   **What**: A concept, a PRD draft, or a "Wouldn't it be cool if..."
*   **Where**: Typically outside the repo (Notion, Slack, verbal).
*   **Output**: A PRD marked `Ready` in Notion.

## Stage 2: Lab (Sandbox)
*   **What**: Experimentation, rough drafts, messy code.
*   **Where**: `/S30-examples/sandbox/` or temporary files.
*   **Rules**:
    *   No review gate needed.
    *   Speed is key.
    *   Use `[DRAFT]` in filenames.

## Stage 3: Production (Governed)
*   **What**: Reliable, reusable code and documentation.
*   **Where**: `/S10-primitives/` (for skills), `/S20-workflows/` (for SOPs).
*   **Rules**:
    *   **Review Gate**: Must pass `S10-primitives/agents.md` Tier 2 check.
    *   **Formatting**: Must follow strict naming conventions.
    *   **Tests**: Must run without errors.

## Stage 4: Banked (Archive)
*   **What**: Finished artifacts, specific run outputs (e.g., "Q3 Report").
*   **Where**: `/S30-examples/banked/YYYY-MM/`.
*   **Rules**:
    *   **Read-Only**: These files should not change.
    *   **Reference**: Use these as "few-shot examples" for future Codex runs.

## Changing Stages
*   **Idea -> Lab**: Clone repo, create context file.
*   **Lab -> Production**: Review, clean up, move file to `S10` or `S20`.
*   **Production -> Banked**: Snapshot specific versions or outputs.
