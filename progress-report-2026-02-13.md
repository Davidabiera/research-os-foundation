# Progress Report: Research OS & 7AIRB Bonus Lesson

**To**: David
**From**: [Your Name]
**Date**: 2026-02-13
**Subject**: DEPLOYED: Foundational Repo Structure & Bonus Lesson Assets

David, per your voice note, the **Foundational Repo is ready to be loaded into any new project today.**

Here is the breakdown of what has been shipped, aligning directly with your directive for "right infrastructure, right primitives."

## 1. The Foundational Repo (Priority #1: Shipped)
> *"I wanna be all set up with like, what is our go to foundational, repo that I can just load in whenever I'm starting a new project."*

**Status**: [x] **DONE** & **PUSHED**
**Location**: `https://github.com/emmanuelsystems/research-os-foundation`

We have established a **Codex-First** architecture that serves as the default OS for all future agentic work.
*   **The Folder System**: We implemented the Semantic Section (`S[XX]`) naming convention to enforce a mental model of "Context -> Primitives -> Workflows -> Assets."
    *   `/S00-foundation/`: The Kernel (Rules & Glossary).
    *   `/S10-primitives/`: The Type System (Agents & Skills).
    *   `/S20-workflows/`: The Standard Operating Procedures.
*   **The Primitives**:
    *   **Agents**: defined in `AGENTS.md` and `S10-primitives/agents.md` (Roles & Permissions).
    *   **Skills**: defined in `S10-primitives/skills.md` and initialized in `.codex/skills/`.
*   **The Operating Loop**: The `README.md` v2 explicitly documents the "Context -> Plan -> Run -> Review -> Bank" loop, ensuring we don't just "chat" but produce reviewable artifacts.

**Action**: You can clone this repo *now* to start any new project.

## 2. Bonus Lesson Content (Priority #2: Ready for Edit)
> *"Developing like... some more engaging content... added as a bonus lesson in the seven day AI readiness boot camp"*

**Status**: [x] **ASSETS READY**
**Location**: `/S90-assets/bonus-lesson-clip-map.md`

We have structured the bonus lesson to be **dynamic** and **concept-driven**, avoiding the "static talking head" trap.
*   **Clip Map**: We have mapped 6 key clips (Jensen/AI Factory, Sam/Scaling, plus new governance concepts) directly to specific files in the repo.
    *   *Example*: Jensen's "AI Factory" clip points users to `S20-workflows/`, reinforcing that "procedures are infrastructure."
*   **Graphics**: Specifications for 3 core visuals (Frontier Stack, Two-Lane Adoption, Operator->Director Shift) are ready in `S90-assets/graphics-specifications.md`.

## 3. Road to Codex Windows (Next Steps)
> *"I would assume that like Windows codex is coming next week... we want to be the ones... designing the custom instructions, the primitives, the aspects of skills"*

With the repo structure locked, we are positioned to:
1.  **Package**: We can now package specific skills (like "Refactoring" or "Research Briefs") into the `.codex/skills` folder.
2.  **Sell**: This repo structure *is* the product. It’s the "shell" we can sell to clients as their started kit.

**Immediate Next Step**:
I will begin drafting the **Mini-Course Outline** (The Bridge) to connect the 7AIRB audience to this new repo-based way of working.
