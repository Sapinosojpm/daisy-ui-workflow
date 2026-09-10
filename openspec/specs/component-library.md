# OpenSpec: DaisyUI Component Library Specification

## Overview
This specification details the standardized DaisyUI component signatures and usage patterns for building consistent UI components across all OpenSpec change proposals.

---

## 1. Buttons (`btn`)

### Class Specifications
- Primary Action: `btn btn-primary`
- Secondary Action: `btn btn-secondary`
- Accent / Brand: `btn btn-accent`
- Ghost / Subdued: `btn btn-ghost`
- Outline Variant: `btn btn-outline btn-primary`
- Destructive Action: `btn btn-error`
- Sizes: `btn-xs`, `btn-sm`, `btn-md` (default), `btn-lg`

### Standard HTML Signature
```html
<button class="btn btn-primary">Save Changes</button>
<button class="btn btn-ghost btn-sm">Cancel</button>
<button class="btn btn-error btn-outline">Delete Item</button>
```

---

## 2. Cards (`card`)

### Class Specifications
- Standard Card Container: `card bg-base-100 shadow-xl border border-base-300`
- Compact Variant: `card card-compact bg-base-100 shadow-md`
- Side Image Variant: `card lg:card-side bg-base-100 shadow-xl`

### Standard HTML Signature
```html
<div class="card bg-base-100 shadow-xl border border-base-300">
  <div class="card-body">
    <h2 class="card-title text-base-content">Card Title</h2>
    <p class="text-base-content/70">Card description and contextual details.</p>
    <div class="card-actions justify-end mt-4">
      <button class="btn btn-primary btn-sm">Action</button>
    </div>
  </div>
</div>
```

---

## 3. Navigation (`navbar` & `menu`)

### Class Specifications
- Navigation Header: `navbar bg-base-100 shadow-sm border-b border-base-300`
- Vertical Sidebar Menu: `menu bg-base-100 w-56 rounded-box`

### Standard HTML Signature
```html
<nav class="navbar bg-base-100 border-b border-base-300 px-4">
  <div class="flex-1">
    <a class="btn btn-ghost text-xl font-bold">AppLogo</a>
  </div>
  <div class="flex-none gap-2">
    <div class="dropdown dropdown-end">
      <div tabindex="0" role="button" class="btn btn-ghost btn-circle avatar">
        <div class="w-10 rounded-full bg-neutral text-neutral-content flex items-center justify-center">
          <span>US</span>
        </div>
      </div>
      <ul tabindex="0" class="menu menu-sm dropdown-content mt-3 z-10 p-2 shadow bg-base-100 rounded-box w-52 border border-base-300">
        <li><a>Profile</a></li>
        <li><a>Settings</a></li>
        <li><a>Logout</a></li>
      </ul>
    </div>
  </div>
</nav>
```

---

## 4. Stats Displays (`stats`)

### Standard HTML Signature
```html
<div class="stats shadow bg-base-100 border border-base-300 w-full">
  <div class="stat">
    <div class="stat-figure text-primary">
      <svg class="inline-block w-8 h-8 stroke-current" fill="none" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
    </div>
    <div class="stat-title">Total Revenue</div>
    <div class="stat-value text-primary">$89,400</div>
    <div class="stat-desc">21% more than last month</div>
  </div>
</div>
```

---

## 5. Modals & Dialogs (`modal`)

### Standard HTML Signature
```html
<!-- Modal Trigger -->
<button class="btn btn-primary" onclick="my_modal_1.showModal()">Open Modal</button>

<!-- Modal Dialog -->
<dialog id="my_modal_1" class="modal">
  <div class="modal-box bg-base-100 border border-base-300">
    <h3 class="font-bold text-lg">Modal Title</h3>
    <p class="py-4">Modal content and confirmation details.</p>
    <div class="modal-action">
      <form method="dialog">
        <button class="btn btn-ghost">Close</button>
        <button class="btn btn-primary">Confirm</button>
      </form>
    </div>
  </div>
</dialog>
```

---

## 6. Form Controls (`input`, `select`, `checkbox`, `toggle`)

### Class Specifications
- Text Input: `input input-bordered w-full max-w-xs focus:input-primary`
- Select Dropdown: `select select-bordered w-full max-w-xs`
- Toggle Switch: `toggle toggle-primary`
- Checkbox: `checkbox checkbox-primary`

---

## 7. Badges & Indicators (`badge`)

### Class Specifications
- Neutral Badge: `badge badge-neutral`
- Primary Badge: `badge badge-primary`
- Success Badge: `badge badge-success`
- Warning Badge: `badge badge-warning`
- Error Badge: `badge badge-error`
- Outline Modifier: `badge badge-outline`
