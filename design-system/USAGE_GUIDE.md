# KodNest Premium Build System - Usage Guide

## Getting Started

Import the design system into your HTML:

```html
<link rel="stylesheet" href="design-system/styles/global.css">
<link rel="stylesheet" href="design-system/layouts/top-bar.css">
<link rel="stylesheet" href="design-system/layouts/context-header.css">
<link rel="stylesheet" href="design-system/layouts/workspace.css">
<link rel="stylesheet" href="design-system/layouts/proof-footer.css">
<link rel="stylesheet" href="design-system/components/buttons.css">
<link rel="stylesheet" href="design-system/components/cards.css">
<link rel="stylesheet" href="design-system/components/inputs.css">
<link rel="stylesheet" href="design-system/components/states.css">
```

## Page Structure Template

Every page follows this structure:

```html
<!-- Top Bar -->
<div class="top-bar">
  <div class="top-bar-left">Project Name</div>
  <div class="top-bar-center">Step 1 / 5</div>
  <div class="top-bar-right">
    <span class="status-badge in-progress">In Progress</span>
  </div>
</div>

<!-- Context Header -->
<div class="context-header">
  <h1 class="context-header-title">Page Title</h1>
  <p class="context-header-subtitle">One-line description of purpose.</p>
</div>

<!-- Workspace Container -->
<div class="workspace-container">
  
  <!-- Primary Workspace (70%) -->
  <div class="primary-workspace">
    <!-- Main content here -->
  </div>

  <!-- Secondary Panel (30%) -->
  <div class="secondary-panel">
    <!-- Instructions and actions here -->
  </div>

</div>

<!-- Proof Footer -->
<div class="proof-footer">
  <div class="proof-checklist">
    <div class="proof-item">
      <div class="proof-checkbox"></div>
      <span>Task 1</span>
    </div>
    <!-- More checklist items -->
  </div>
</div>
```

## Component Examples

### Buttons

```html
<button class="btn btn-primary">Primary Action</button>
<button class="btn btn-secondary">Secondary Action</button>
```

### Cards

```html
<div class="card">
  <div class="card-header">
    <h3 class="card-title">Card Title</h3>
    <p class="card-subtitle">Card description</p>
  </div>
  <div class="card-body">
    <!-- Content -->
  </div>
</div>
```

### Inputs

```html
<label class="label">Field Label</label>
<input type="text" class="input" placeholder="Enter value">
```

### Error State

```html
<div class="error-state">
  <h3 class="error-state-title">Something went wrong</h3>
  <p class="error-state-message">The build failed due to a syntax error.</p>
  <p class="error-state-solution">Check line 42 in app.js and fix the missing semicolon.</p>
  <button class="btn btn-primary">Try Again</button>
</div>
```

### Empty State

```html
<div class="empty-state">
  <h3 class="empty-state-title">No projects yet</h3>
  <p class="empty-state-message">Create your first project to get started.</p>
  <div class="empty-state-action">
    <button class="btn btn-primary">Create Project</button>
  </div>
</div>
```

## Design Tokens

Access design tokens via CSS variables:

```css
/* Colors */
var(--color-background)
var(--color-text-primary)
var(--color-accent)

/* Spacing */
var(--space-1) /* 8px */
var(--space-2) /* 16px */
var(--space-3) /* 24px */
var(--space-4) /* 40px */
var(--space-5) /* 64px */

/* Typography */
var(--font-serif)
var(--font-sans)
var(--text-base)
var(--leading-relaxed)
```

## Rules

1. Use only the defined spacing scale
2. Stick to the 4-color palette
3. Follow the global layout structure
4. Maintain visual consistency
5. No custom animations or effects
