## Context

See `proposal.md` for background motivation. The existing workspace includes OpenSpec specifications and a prototype UI (`index.html`). To make the workflow specifically focused on UI redesigns, we need a technical structure for comparing legacy UI components against refactored DaisyUI primitives and performing theme audit checks.

## Goals / Non-Goals

**Goals:**
- Provide a clear refactoring architecture for transforming custom/raw CSS into semantic DaisyUI components.
- Implement an interactive "Redesign Sandbox" in `index.html` featuring side-by-side comparison tabs ("Legacy View" vs. "DaisyUI Redesigned View").
- Update OpenSpec configuration to include redesign-focused guidance during `proposal`, `specs`, `apply`, and `archive` operations.

**Non-Goals:**
- Building automated AST CSS parsers or CLI conversion tools (the workflow focuses on human + AI spec-driven refactoring).

## Decisions

### Decision 1: Interactive Redesign Sandbox Component in `index.html`
- **Choice**: Implement a tabbed preview component using DaisyUI `tabs tabs-lifted` inside `index.html`.
- **Rationale**: Allows developers and design reviewers to visually toggle between unstyled/legacy raw markup and refactored DaisyUI semantic components within the exact same theme runtime context.
- **Alternatives Considered**: Creating separate `.html` files for legacy and redesigned versions. Rejected because cross-file navigation hampers quick visual comparison and theme testing.

### Decision 2: Redesign Specification Template Standards
- **Choice**: Structure redesign delta specs with explicit "Legacy State" vs. "Redesigned DaisyUI State" mapping tables under requirement scenarios.
- **Rationale**: Provides clear contract boundary for AI assistants during `/opsx:apply` to ensure no functional props or ARIA labels are dropped.

## Risks / Trade-offs

- **[Risk]**: Custom CSS specificity conflicts if legacy styles are left in global stylesheets.
  - **Mitigation**: Isolate legacy sandbox markup inside scoped CSS blocks or inline baseline styling in the sandbox component.
