## Why

When performing UI redesigns (e.g., migrating custom utility CSS/legacy components to DaisyUI, updating visual themes, or refactoring layouts), developers need a structured spec-driven process to ensure component parity, visual consistency, and theme safety without breaking existing component contracts.

This change enhances the OpenSpec DaisyUI workflow specifically for **UI Redesign tasks** by introducing visual diff standards, component refactoring guidelines, interactive redesign sandboxes, and theme audit requirements.

## What Changes

- **Redesign Workflow Specification**: Define formal rules for scoping UI redesigns, mapping legacy components to DaisyUI primitives, and auditing color themes.
- **Interactive Component Redesign Sandbox**: Enhance the prototype workspace with a side-by-side redesign preview comparing legacy CSS/raw layouts against DaisyUI refactored components.
- **Visual & Theme Audit Guidelines**: Introduce requirements for verifying theme switching (`data-theme`) and responsive layout parity during redesigns.

## Capabilities

### New Capabilities
- `ui-redesign-process`: Establishes requirements for UI redesign workflows, legacy component mapping, theme compatibility auditing, and side-by-side visual verification.

### Modified Capabilities
<!-- None -->

## Impact

- **OpenSpec Specifications**: New capability spec `specs/ui-redesign-process/spec.md`.
- **UI Workspace**: Interactive redesign sandbox added to `index.html`.
- **Developer Workflow**: Enhanced guidelines for redesign proposals and task execution.

## Non-Goals
- Automatic CSS-to-DaisyUI AST transpiler (manual spec-driven refactoring guided by AI).
