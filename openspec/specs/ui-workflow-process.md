# OpenSpec: Spec-Driven UI Design Workflow Process

## Overview
This specification details the end-to-end lifecycle for planning, proposing, implementing, verifying, and archiving UI designs using **OpenSpec** and **DaisyUI**.

---

## The 5-Stage Spec-Driven UI Design Lifecycle

```
┌─────────────────┐     ┌─────────────────┐     ┌──────────────────┐     ┌──────────────────┐     ┌──────────────────┐
│  1. EXPLORE     │ ──> │  2. PROPOSE     │ ──> │  3. APPLY        │ ──> │  4. VERIFY       │ ──> │  5. ARCHIVE      │
│  Brainstorm UI  │     │  Write Specs    │     │  Implement Code  │     │  Test & Preview  │     │  Update Main     │
│  & Mockups      │     │  & Tasks        │     │  DaisyUI Layout  │     │  Theme & Mobile  │     │  Specs           │
└─────────────────┘     └─────────────────┘     └──────────────────┘     └──────────────────┘     └──────────────────┘
```

---

## Stage Details & Commands

### Stage 1: Explore (`/opsx:explore` or `openspec-explore` skill)
- **Goal**: Brainstorm layout structures, select DaisyUI components, determine color theme constraints, and identify key user interactions.
- **Output**: Informal architectural notes or layout rough draft.

### Stage 2: Propose (`/opsx:propose <feature-name>` or `openspec-propose` skill)
- **Goal**: Formally generate a change proposal folder under `openspec/changes/<feature-name>/`.
- **Required Artifacts**:
  1. `proposal.md`: Executive summary of why the UI is needed, visual mockups/structure, DaisyUI component list, and non-goals.
  2. `specs/<delta-spec>.md`: Delta specification detailing exact DaisyUI component HTML classes, theme token usage, responsive breakpoints, and interactive state triggers.
  3. `tasks.md`: Sequenced checklist of implementation steps.

### Stage 3: Apply (`/opsx:apply` or `openspec-apply-change` skill)
- **Goal**: Execute the tasks outlined in `tasks.md`.
- **Guidelines**:
  - Implement HTML structure using DaisyUI semantic classes (`btn`, `card`, `navbar`, `stats`, `modal`, `drawer`).
  - Use DaisyUI semantic color classes (`bg-base-100`, `text-primary`, etc.) instead of hardcoded hex values.
  - Implement dynamic `data-theme` switching logic.

### Stage 4: Verify
- **Goal**: Inspect visual presentation and automated validity.
- **Commands**:
  - `npx openspec validate`: Ensures change proposals adhere to schema rules.
  - Preview HTML/CSS in browser to test responsive breakpoints (`sm`, `md`, `lg`, `xl`) and themes (`dark`, `light`, `cupcake`, `cyberpunk`).

### Stage 5: Archive (`/opsx:archive` or `openspec-archive-change` skill)
- **Goal**: Finalize the change. Merge delta specs into the main specifications in `openspec/specs/` and move the change proposal to `.openspec/archive/`.
- **Command**: `npx openspec archive <feature-name>`
