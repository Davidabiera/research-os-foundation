# Project Context: Research OS Foundation

- **Status:** draft
- **Owner:** foundation-maintainers
- **Last Updated:** 2026-02-17

## PRD Content

# Product Requirements Document (PRD)

- **Status:** draft
- **Owner:** foundation-maintainers
- **Last Updated:** 2026-02-17

## 1. Document Control
- **Project Name:** research-os-foundation
- **Owner:** foundation-maintainers
- **Contributors:** operations-agent, builder-agent
- **Version:** v0.1.0
- **Decision State:** draft

## 2. PRD Source Traceability
- **Primary Source:** Repository README and foundation architecture
- **Supporting Sources:** Agent entrypoint and delivery progress report
- **Source Links / File Paths:** `README.md`, `AGENTS.md`, `progress-report-2026-02-13.md`

## 3. Problem Statement
Teams using AI often produce outputs in chat that are hard to review, reuse, and scale. A shared, repeatable operating model is needed so both humans and agents can create durable project artifacts with clear process and governance.

## 4. Goals
- Provide a standard repository structure for agentic project execution.
- Define reusable primitives, workflows, and examples that reduce startup ambiguity.
- Ensure each run produces reviewable files and a traceable run ledger.

## 5. Non-Goals
- Building one specific product feature set.
- Replacing project-specific implementation repositories.

## 6. Users and Stakeholders
- **Primary User(s):** Operators and builders starting new AI-assisted projects
- **Secondary User(s):** Reviewers, QA contributors, and team leads
- **Stakeholders / Decision Makers:** Foundation maintainers and project owners

## 7. Scope
### In Scope
- Semantic section structure (`S00`, `S10`, `S20`, `S30`, `S90`)
- Agent entrypoint and execution directives
- Startup and execution workflows
- Example artifacts and save/bank policy

### Out of Scope
- Domain-specific application logic for downstream projects
- Vendor-specific deployment automation

## 8. Requirements
### Functional Requirements
1. Provide workflow guides for trigger-to-repo and context-to-output execution.
2. Enforce artifact-first operation where outputs are saved to files.
3. Include a run ledger schema for traceability across runs.

### Non-Functional Requirements
- Performance: New projects can be initialized in one working session.
- Reliability: Workflows are explicit, deterministic, and reproducible.
- Security/Privacy: Sensitive sections require permission boundaries.
- Accessibility: Markdown-first, human-readable, agent-legible structure.
- Maintainability: Living files carry status/owner/update metadata.

## 9. Success Metrics
- Startup artifacts exist for each initialized project (target: 100%).
- Run ledger entry coverage after each run (target: 100%).
- Time to first executable run from new idea (target: under 30 minutes).

## 10. Constraints
- Technical constraints: Markdown-centric system with codified folder semantics.
- Time constraints: Must support rapid bootstrap from trigger input.
- Resource constraints: Designed for small teams with mixed human/agent operation.
- Compliance constraints: Follow section-level governance and promotion rules.

## 11. Risks and Mitigations
- **Risk:** Workflow non-compliance leads to inconsistent outputs.
  **Mitigation:** Keep explicit workflow steps and quality gates in `S20-workflows/`.
- **Risk:** Knowledge stays in chat and is not reusable.
  **Mitigation:** Enforce artifact generation and save/bank process.

## 12. Dependencies
- Internal: `AGENTS.md`, `S10-primitives/`, `S20-workflows/`
- External: Git provider/repository hosting for collaboration and version control

## 13. Milestones
- M1: Foundation repo bootstrapped and reviewed.
- M2: First project initialized from PRD using trigger-to-repo workflow.
- M3: Reusable outputs promoted to banked examples and workflows.

## 14. Open Questions
1. Which automations should be added first for trigger ingestion?
2. What minimal rubric should gate promotion to banked state?
3. Which default stack-specific `.gitignore` variants should be provided?

## 15. Initial Artifact Plan
- `README.md`
- `S00-foundation/prd.md`
- `S20-workflows/project-plan.md`
- `S20-workflows/run-ledger.md`
- `.gitignore`
- `src/`
- `tests/`

## 16. Approval
- **Reviewer:** pending
- **Decision:** draft
- **Date:** 2026-02-17
- **Notes:** Initialized baseline artifacts from existing foundation context.
