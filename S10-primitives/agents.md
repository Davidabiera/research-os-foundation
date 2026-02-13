# Agents

## Purpose
This document defines the roles, capabilities, and operational constraints of agents within the system, treating them as specialized, tiered entities designed for modular execution.

## Agent Roles

### Research Agent
*   **Function**: Gathers, cites, and summarizes relevant information.
*   **Key Responsibilities**:
    *   Find and cite primary sources.
    *   Summarize key findings.
    *   Create context for downstream tasks.

### Builder Agent
*   **Function**: Creates artifacts, drafts code, and implements designs.
*   **Key Responsibilities**:
    *   Write initial drafts of documents.
    *   Implement code or configurations.
    *   Create visual or functional assets.

### QA Agent
*   **Function**: Checks artifacts against a predefined rubric for correctness and quality.
*   **Key Responsibilities**:
    *   Validate builder output.
    *   Verify compliance with specifications.
    *   Enforce quality standards.

## Permission Tiers

### Tier 0: No External Actions
*   **Capabilities**: Text-only output, simulations, internal reasoning.
*   **Permissions**: Cannot access external systems or execute changes.

### Tier 1: Read-Only Tools
*   **Capabilities**: Can read from documentation, drive, and public web sources.
*   **Permissions**: Cannot modify external state.
*   **Tools**: Search, `read_file`, `list_dir`.

### Tier 2: Write Actions with Review Gate
*   **Capabilities**: Can modify system state, write files, and execute deployment actions.
*   **Permissions**: Restricted to actions pre-approved by a human reviewer or designated higher-tier agent.
*   **Gate**: Requires explicit approval for destructive or state-changing operations.

## Side Effect Rules
The goal is to avoid unintended consequences (e.g., the "Slack marks as read" problem) and ensure system integrity.

1.  **Use Agent Accounts**: Whenever possible, use dedicated service accounts for agent interactions, not personal user accounts.
2.  **Prefer Read-Only Integrations**: Default to read-only access unless write access is strictly necessary for the defined task.
3.  **Require Approval for State Changes**: Any action that modifies external systems (e.g., posting a comment, deleting a file) must be gated behind an approval mechanism.
4.  **Audit Trail Requirements**:
    *   **Every Run Produces an Artifact**: Log all actions, decisions, and outputs in a retrievable format.
    *   **Every Artifact Has a Reviewer and Date**: Ensure accountability by tracking who reviewed the output and when.
