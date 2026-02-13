# Skills

## Skill Definition
A skill is a reusable, atomic unit of work defined by specific instructions, inputs, and expected outputs. It acts as a standardized process for agents to execute reliably without drift.

## Skill Format Template

### Purpose
*   **Definition**: The primary goal and function of this skill.
*   **Scope**: What it covers and what it does not.

### Inputs
*   **Requirements**: Necessary data, context, or files to begin execution.
*   **Format**: Defined schemas or file types.

### Outputs (Artifact Format)
*   **Deliverables**: The tangible results produced by executing the skill (e.g., markdown file, code snippet, report).
*   **Structure**: Required format or naming convention.

### Steps
1.  **Step-by-step instructions**: Clear, actionable items for the agent to perform.

### Stop Rules
*   **Completion Criteria**: How to know when the skill has successfully finished.
*   **Error Handling**: What to do if inputs are missing or invalid.

### Review Checklist
*   [ ] Verify all required inputs were processed.
*   [ ] Confirm the output matches format specifications.
*   [ ] Check for accuracy and adherence to constraints.

### Examples
*   **Sample usage**: Demonstrate how to invoke the skill with sample inputs and outputs.

## Skill Routing Rules
### When to Use
*   Use this skill when you have a defined input and require a standardized output.
*   When executing repetitive or structured tasks.

### When Not to Use
*   Do not use this skill for open-ended exploration without defined constraints.
*   When the task requires significant creative deviation from the standard process.

## Versioning Rule
Every edit **increments a version number** to ensure consistency and traceability.

### Changelog Line
*   **Format**: `v1.0.0 (YYYY-MM-DD): Initial release.`
*   **Entry**: Detailed description of what changed and why.
