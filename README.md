# DaisyUI + OpenSpec Spec-Driven UI Design Workflow

A complete Spec-Driven UI Design Workflow repository using **OpenSpec** (`@fission-ai/openspec`) and **DaisyUI** (Tailwind CSS component library).

## 🚀 Quick Start

1. **Clone the repository**:
   ```bash
   git clone git@github.com:Sapinosojpm/daisy-ui-workflow.git
   cd daisy-ui-workflow
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Preview the Interactive Dashboard**:
   Open [`index.html`](index.html) in your browser to test the DaisyUI component layout, live theme switcher (`dark`, `light`, `cupcake`, `cyberpunk`, `synthwave`, `nord`), stats grid, zebra table, responsive sidebar drawer, and modal dialog.

---

## 🎨 OpenSpec Specifications Structure

- [`openspec/config.yaml`](openspec/config.yaml): Project context, tech stack rules, and DaisyUI per-artifact guidelines.
- [`openspec/specs/ui-design-system.md`](openspec/specs/ui-design-system.md): Theme tokens (`data-theme`), semantic color hierarchy (`primary`, `secondary`, `accent`, `base-100/200/300`), typography, and grid shells.
- [`openspec/specs/component-library.md`](openspec/specs/component-library.md): Standard HTML class signatures for buttons, cards, navbars, drawers, stats, tables, badges, and modals.
- [`openspec/specs/ui-workflow-process.md`](openspec/specs/ui-workflow-process.md): 5-stage UI design lifecycle specification.

---

## 🔄 The 5-Stage UI Workflow Loop

1. **Explore** (`/opsx:explore`): Brainstorm UI requirements, layout structures, and DaisyUI components.
2. **Propose** (`/opsx:propose <feature-name>`): Auto-generate change proposal (`proposal.md`, `specs/.../spec.md`, `tasks.md`).
3. **Apply** (`/opsx:apply`): Implement DaisyUI code and layout HTML.
4. **Verify**: Run `npx openspec validate --all` to ensure schema compliance and test themes in browser.
5. **Archive** (`npx openspec archive <feature-name>`): Merge completed delta specs into core persistent specifications.

---

## 🛠️ CLI Commands

```bash
# Validate OpenSpec project compliance
npx openspec validate --all

# View active change status
npx openspec status --change analytics-dashboard

# List all persistent specs
npx openspec list --specs
```

---

## 📄 License

ISC License
