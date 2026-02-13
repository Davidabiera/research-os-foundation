# Example: Research Brief - "Adopting Agentic Coding"

**Status**: [DRAFT | REVIEW | APPROVED]
**Date**: 2026-02-13
**Author**: [Your Name]
**Reviewer**: [Reviewer Name]

## 1. Goal
Evaluate the current landscape of "Agentic Coding" tools and define a strategy for team adoption in Q2.

## 2. Context & Constraints
*   **Context**: The team is currently using GitHub Copilot but finding limitations in multi-file refactoring. new tools like Cursor, Windsurf, and Roo are emerging.
*   **Constraints**:
    *   Must integrate with existing VS Code setup.
    *   Must not compromise proprietary code security.
    *   Budget cap: $50/user/month.

## 3. Plan
1.  **Survey**: Identify top 3 tools based on community sentiment (Twitter, Reddit, hacker news).
2.  **Trial**: Run a 1-week pilot with 2 senior engineers using the top tool.
3.  **Evaluate**: Score against criteria: latency, context window, security, price.
4.  **Recommend**: Produce a 1-page decision memo.

## 4. Execution Log
*   **2026-02-14 (Survey)**: Identified Cursor and Windsurf as leaders. Dismissed smaller tools due to lack of enterprise support.
*   **2026-02-16 (Trial)**: Installed Cursor. Initial impression: "Composer" feature is a game changer for multi-file edits.
*   **2026-02-18 (Security Check)**: Confirmed "Privacy Mode" prevents code from being used for training models.

## 5. Decision Delta
*   **Decision**: Adopt Cursor for the senior team immediately.
*   **Why**: The productivity gain in refactoring existing legacy modules outweighs the learning curve. The cost is within budget.
*   **Rejected Alternative**: Building a custom internal tool. Too high maintenance for current team size.

## 6. Learing Bank (for future reference)
*   **Insight**: "Context" is not just open files; it's also recent terminal history. Tools that read terminal output solve bugs faster.
*   **Prompt Pattern**: "Don't just fix the line, explain *why* it broke first." This prevents "blind" fixes.

## 7. Next Steps
*   [ ] Purchase 5 seats.
*   [ ] Schedule 30-min onboarding demo.
*   [ ] Update `/S10-primitives/skills.md` with "Refactoring with Agents" standard operating procedure.
