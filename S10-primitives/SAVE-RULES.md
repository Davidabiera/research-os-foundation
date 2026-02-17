# Codex Save Rules

These rules dictate how **Codex agents** must name, locate, and save files. Compliance is mandatory for all automated outputs.

## 1. Naming Convention
*   **Format**: `YYYY-MM-DD-kebab-case-name.md` (or `.py`, `.json`, etc.)
*   **Case**: Lowercase kebab-case only. No spaces.
*   **Date Prefix**: Mandatory for logs, reports, and time-sensitive outputs. Optional for stable source code files.
*   **Examples**:
    *   `2026-02-16-daily-standup.md`
    *   `utils.py` (stable source)
    *   `api-spec-v1.json`

## 2. Default Save Locations
Unless specified otherwise by a Workflow or Prompt:

*   **Context / Input**: `/S00-foundation/`
*   **Drafts / Sandbox**: `/S30-examples/sandbox/`
*   **Final Output**: Typically `/S30-examples/` or a project-specific `src/` folder if defined.
*   **Logs**: `/S90-assets/logs/`

## 3. Versioning
*   **Never overwrite** a file unless explicitly instructed.
*   **Append**: If updating a log, append to the existing file.
*   **Version Up**: If modifying a significant artifact, create a new version:
    *   `file-v1.md` -> `file-v2.md`
    *   `report-draft.md` -> `report-final.md`

## 4. The Landing Zone
If Codex is unsure where to put a file:
1.  Check for a `temp/` or `scratch/` folder.
2.  If none exists, create `S30-examples/sandbox/` and save it there.
3.  **ALWAYS** notify the user of the saved location in the final response.

## 5. Content Structure
Every markdown artifact should start with a YAML frontmatter block or a header block containing:
```markdown
# Title
**Date**: YYYY-MM-DD
**Author**: Codex (Agent: [Role])
**Status**: [DRAFT | REVIEW | FINAL]
```
