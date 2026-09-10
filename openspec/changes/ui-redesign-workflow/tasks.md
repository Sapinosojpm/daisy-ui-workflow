## 1. OpenSpec Redesign Specification & Rules

- [ ] 1.1 Update `openspec/config.yaml` to include explicit guidance for UI redesign proposals, legacy component mapping, and multi-theme audits. Verify configuration syntax with `npx openspec validate --all`.
- [ ] 1.2 Add the core `specs/ui-redesign-process.md` specification defining legacy refactoring requirements and theme audit standards. Verify with `npx openspec validate --all`.

## 2. Interactive Redesign Sandbox Implementation

- [ ] 2.1 Implement the side-by-side Redesign Sandbox container in `index.html` using DaisyUI `tabs tabs-lifted` components. Verify layout rendering in browser preview.
- [ ] 2.2 Add legacy unstyled markup and refactored DaisyUI semantic components (`card`, `btn`, `stats`, `badge`) into the sandbox comparison tabs. Verify visual toggling between Legacy and Redesigned modes.
- [ ] 2.3 Verify dynamic `data-theme` switching (`dark`, `light`, `cupcake`, `cyberpunk`, `synthwave`, `nord`) across all sandbox components without hex color leakage.

## 3. Validation & Quality Check

- [ ] 3.1 Run `npx openspec validate --all` to ensure zero validation errors across all active change proposals.
- [ ] 3.2 Verify responsive layout behavior on mobile, tablet, and desktop viewports.
