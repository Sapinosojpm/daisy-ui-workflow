# OpenSpec: DaisyUI Design System Specification

## Overview
This specification defines the foundational visual architecture, theme tokens, typography, and responsive layout standards for all user interfaces built in this project using **DaisyUI** and **Tailwind CSS**.

---

## 1. Theme Strategy & Semantic Color Tokens

### Theme Controller (`data-theme`)
All pages must support theme switching via the `data-theme` HTML attribute on `<html>`:
```html
<html data-theme="dark">
```

Standard supported themes:
- `light` (Default light design)
- `dark` (High-contrast dark mode)
- `cupcake` (Pastel branding theme)
- `cyberpunk` (Vibrant tech theme)

### Semantic Color Hierarchy
Never use hardcoded hex colors or arbitrary raw color utilities like `bg-[#123456]`. Use DaisyUI's semantic color system:

| Semantic Token | Purpose | DaisyUI Background Class | Text Class |
| :--- | :--- | :--- | :--- |
| **Base 100** | Primary page background | `bg-base-100` | `text-base-content` |
| **Base 200** | Secondary background (cards, sidebars) | `bg-base-200` | `text-base-content` |
| **Base 300** | Surface / Header / Border background | `bg-base-300` | `text-base-content` |
| **Primary** | Main action button, active brand highlights | `bg-primary` | `text-primary-content` |
| **Secondary** | Supporting call-to-action | `bg-secondary` | `text-secondary-content` |
| **Accent** | Special highlights, badges, promo elements | `bg-accent` | `text-accent-content` |
| **Neutral** | Dark backgrounds, footer, dark containers | `bg-neutral` | `text-neutral-content` |
| **Info** | Informational notices, help alerts | `bg-info` | `text-info-content` |
| **Success** | Success state, positive metrics | `bg-success` | `text-success-content` |
| **Warning** | Warning state, cautions | `bg-warning` | `text-warning-content` |
| **Error** | Critical error state, danger actions | `bg-error` | `text-error-content` |

---

## 2. Responsive Layout Architecture

### Container & Breakpoint Standards
- Mobile (`< 640px`): Single column (`grid-cols-1`), stacked navigation, collapsible drawer.
- Tablet (`sm: 640px` / `md: 768px`): 2-column layout (`grid-cols-2`), compact navigation bar.
- Desktop (`lg: 1024px` / `xl: 1280px`): Full dashboard layout (`grid-cols-12`), expanded sidebar drawer, wide container (`max-w-7xl`).

### Layout Shell Template
```html
<div class="drawer lg:drawer-open min-h-screen bg-base-200">
  <input id="app-drawer" type="checkbox" class="drawer-toggle" />
  <div class="drawer-content flex flex-col">
    <!-- Navbar -->
    <header class="navbar bg-base-100 shadow-sm border-b border-base-300 px-4">
      ...
    </header>
    <!-- Main Content -->
    <main class="p-6 flex-1 max-w-7xl w-full mx-auto">
      ...
    </main>
  </div>
  <!-- Sidebar -->
  <div class="drawer-side">
    <label for="app-drawer" class="drawer-overlay"></label>
    <aside class="menu p-4 w-80 min-h-full bg-base-100 text-base-content border-r border-base-300">
      ...
    </aside>
  </div>
</div>
```

---

## 3. Typography & Elevation

### Headings
- Hero / Page Title: `text-3xl font-bold tracking-tight text-base-content`
- Section Title: `text-xl font-semibold text-base-content`
- Card Title: `card-title text-lg font-medium`

### Shadows & Elevation
- Subtle Card: `shadow-sm`
- Floating Card / Panel: `shadow-md` or `shadow-lg`
- Modal / Popover: `shadow-2xl`
