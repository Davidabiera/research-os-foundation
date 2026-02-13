# Graphics Specifications for Bonus Lesson

Since direct image generation is currently unavailable, this document provides detailed specifications and conceptual diagrams for the 3 core graphics required for the 7AIRB Bonus Lesson.

## 1. Frontier Stack Overview
**Goal**: Visualize the 4 layers of a modern AI system.

**Visual Style**:
*   **Structure**: 4 horizontal layers, stacked like a cake or server rack.
*   **Colors**: Deep, rich gradients (Cyberpunk/Enterprise fusion).
    *   Bottom (Foundation): Deep Blue/Indigo
    *   Middle-Low (Action): Teal/Cyan
    *   Middle-High (Quality): Purple/Violet
    *   Top (Identity): Magenta/Pink
*   **Icons**: Minimalist, white line art on the left side of each bar.

**Content**:
1.  **(Top) Identity**: Who is acting? (Roles, Permissions, Memory)
2.  **(Upper Middle) Eval**: Is it good? (Rubrics, Omni-Reviewers)
3.  **(Lower Middle) Execution**: Doing the work. (Tools, Loops, APIs)
4.  **(Bottom) Context**: What do we know? (RAG, Files, State)

**Mermaid Diagram Concept**:
```mermaid
graph BT
    Context[Context (Foundation)] --> Execution[Execution (Action)]
    Execution --> Eval[Eval (Quality Control)]
    Eval --> Identity[Identity (Roles & Permissions)]
    style Context fill:#1a237e,stroke:#fff,color:#fff
    style Execution fill:#006064,stroke:#fff,color:#fff
    style Eval fill:#4a148c,stroke:#fff,color:#fff
    style Identity fill:#880e4f,stroke:#fff,color:#fff
```

## 2. Two-Lane Adoption Model
**Goal**: Show the safety of the "Sandbox" vs. the reliability of the "Governed Lane".

**Visual Style**:
*   **Structure**: A road splitting into two distinct paths.
*   **Left Lane (Sandbox)**:
    *   **Visual**: Winding, colorful, slightly chaotic. Icons of lightbulbs, sparks, "messy" papers.
    *   **Label**: "Sandbox Mode"
    *   **Purpose**: Experimentation, low stakes, high speed.
*   **Right Lane (Governed)**:
    *   **Visual**: Straight, paved, secure. Has a "Gate" icon (toll booth or shield) at the entry.
    *   **Label**: "Production Lane"
    *   **Purpose**: Reliable, repeatable, high stakes.
*   **Connection**: Arrows showing successful experiments moving from the Sandbox -> passing the Gate -> entering Production.

**Concept Text**:
"Chaos in the Sandbox, Order in Production. The Gate makes the difference."

## 3. Operator to Director Role Shift
**Goal**: Illustrate the change in the human's role when using agents.

**Visual Style**:
*   **Left Side (Operator)**:
    *   **Image**: Silhouette of a person hunched over a keyboard, typing frantically.
    *   **Sursum**: Surrounded by code blocks, terminal windows, emails.
    *   **Label**: "Operator (Doing)"
*   **Transition**: An arrow transforming the figure.
*   **Right Side (Director)**:
    *   **Image**: Silhouette of a person standing, conducting (like an orchestra) or reviewing a blueprint.
    *   **Sursum**: Surrounded by Agent icons, clean checklists, "Approved" stamps.
    *   **Label**: "Director (Defining)"

**Key Visual Metaphor**:
Moving from *typing the code* to *reviewing the PR*.
Moving from *writing the copy* to *approving the campaign*.
