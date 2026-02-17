# Trigger Spec: Notion to Repo

This document defines the data structure and events required to automate project creation.

## 1. The Source: Notion PRD
Required fields for the "Projects" database in Notion.

| Field Name | Type | Options | Purpose |
| :--- | :--- | :--- | :--- |
| **Project Name** | Title | - | Becomes the Repo Name (kebab-case). |
| **Status** | Status | Idea, Ready to Build, In Progress, Banked | The trigger event. |
| **Owner** | Person | - | Who to assign the repo to. |
| **Goal** | Text | - | Context for `README.md`. |
| **Type** | Select | Research, Product, Content | Determines which template to use. |

## 2. The Trigger Event
*   **Condition**: Status changes from `Idea` -> `Ready to Build`.
*   **Action**: Fire webhook to Automation Service (Zapier/Make).

## 3. Automation Payload
The automation script receives this JSON:
```json
{
  "project_name": "foundation-repo-v1",
  "owner_email": "emmanuel@example.com",
  "goal": "Create a foundational repo structure...",
  "type": "Product",
  "notion_id": "12345-abcde"
}
```

## 4. Repo Actions (The "Hydration")
Upon receiving the payload, the automation (or Codex Agent) must:
1.  **Clone Foundation**: Copy `emmanuelsystems/research-os-foundation` to `emmanuelsystems/foundation-repo-v1`.
2.  **Update README**: Replace the generic title with the `project_name` and `goal`.
3.  **Create Context**: Create `S00-foundation/context.md` containing the full Notion PRD content.
4.  **Link Back**: Post the new Repo URL back to the Notion Page properties.

## 5. Manual Fallback (Until Automation is Live)
1.  Copy the Notion PRD content.
2.  Run `git clone [foundation-url] [new-project-name]`.
3.  Paste content into `S00-foundation/context.md`.
4.  Commit and Push.
