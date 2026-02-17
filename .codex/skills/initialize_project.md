---
name: initialize_project
description: "Hydrate a new repository with project-specific details from a PRD."
---

# Initialize Project

## Purpose
This skill transforms a generic "Research OS Foundation" repo into a specific project workspace by applying details from the Project Requirements Document (PRD).

## Inputs
*   **PRD Content**: The full text of the PRD (from Notion, Context file, or User input).
*   **Repo Name**: The desired name of the project.

## Outputs
*   Updated `README.md`
*   Created `S00-foundation/context.md`
*   Initialized `task.md`

## Steps
1.  **Analyze PRD**: Read the provided PRD content to extract:
    *   Project Name
    *   Goal / Objective
    *   One-line Summary
    *   Key Stakeholders

2.  **Create Context**:
    *   Create a new file: `S00-foundation/context.md`.
    *   Paste the full PRD content into this file.
    *   Add a header: `# Project Context: [Project Name]`.

3.  **Update README**:
    *   Read `README.md`.
    *   Replace the title `# Research OS Foundation` with `# [Project Name]`.
    *   Replace the generic description with the "One-line Summary" and "Goal" extracted from the PRD.
    *   Keep the "Folder Map" and "Operating Loop" sections intact (they are universal).

4.  **Initialize Task List**:
    *   Create a `task.md` file in the root (or update if exists).
    *   Add the first task: `- [ ] Initialize Project structure and context`.

## Stop Rules
*   Do not overwrite `S10-primitives/` or `S20-workflows/` files.
*   If `S00-foundation/context.md` already exists, ask before overwriting.
