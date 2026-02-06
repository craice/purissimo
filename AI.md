# Purissimo — AI Instructions

## Project Overview

Purissimo is a minimalist design system built with pure HTML5 and CSS — zero JavaScript in components. The name comes from Italian "purest."

**Tagline:** "Less is pure"

**Author:** Rafael Craice

## Key Files

- `SPECIFICATION.md` — Complete design system specification (design tokens, components, philosophy)
- `DEVELOPMENT_ROADMAP.md` — Phased task list with checklist and logs

**Always read these files before starting any work.**

## Core Principles (Never Violate)

1. **No JavaScript** — Components must work with HTML + CSS only
2. **Accessibility first** — WCAG 2.1 AA minimum, proper ARIA, keyboard navigation
3. **Single CSS file** — All styles go in `purissimo.css`
4. **Base-4 spacing** — Use the spacing tokens (multiples of 4px)
5. **Semantic HTML** — Use proper HTML5 elements

## Tech Stack

- HTML5
- CSS (modern features allowed: custom properties, grid, flexbox, `:has()`, `@layer`, `@container`)
- Google Fonts: Outfit, Material Symbols Outlined
- No build tools required
- Hosting: GitHub Pages

## File Structure

```
purissimo/
├── purissimo.css           # Main CSS file
├── purissimo.min.css       # Minified production version
├── index.html              # Landing page + Documentation
├── catalog.html            # Component catalog / storybook
├── examples.html           # Component composition recipes
├── AI.md                   # This file
├── SPECIFICATION.md        # Design specification
├── DEVELOPMENT_ROADMAP.md  # Task list and logs
├── README.md               # Project readme
├── LICENSE                 # MIT License
└── examples/
    └── template.html       # Starter template
```

## CSS Organization

Use `@layer` for cascade management:

```css
@layer reset, tokens, base, components, utilities;
```

## Naming Conventions

- **Components:** `.component-name` (kebab-case)
- **Variants:** `.component-name--variant` (BEM modifier)
- **Children:** `.component-name__child` (BEM element)
- **Utilities:** `.utility-name`

Examples:
- `.btn`, `.btn--primary`, `.btn--lg`
- `.card`, `.card__header`, `.card__body`, `.card--elevated`
- `.form-input`, `.form-label`, `.form-checkbox__indicator`

## Color Palette Reference

Primary colors (Antarctic ice theme):
- `--pure-white: #FFFFFF`
- `--ice-white: #F8FAFB`
- `--frost: #EEF3F6`
- `--glacial-500: #2E9CAA` (primary action color)

Always use CSS variables, never hardcoded colors.

## Working Process

1. **Before starting a phase:** Read the relevant section in SPECIFICATION.md
2. **During development:** Follow the task list in DEVELOPMENT_ROADMAP.md
3. **After completing tasks:** 
   - Mark tasks as `[x]` in DEVELOPMENT_ROADMAP.md
   - Add entry to Execution Log with date, time, and summary
   - Log any decisions in AI Decision Log

## Logging Requirements

### Execution Log Format
```markdown
| Date | Time | Summary |
|------|------|---------|
| 2024-01-15 | 14:30 | Completed all button components with variants and states |
```

### AI Decision Log Format
```markdown
| Date | Time | Phase/Task | Decision | Rationale |
|------|------|------------|----------|-----------|
| 2024-01-15 | 14:35 | 3.4 | Used `gap` instead of margins for button icon spacing | Better alignment, fewer properties to manage |
```

**Log decisions when:**
- Choosing between multiple valid approaches
- Specs are ambiguous
- Adding something not explicitly defined
- Making performance/compatibility tradeoffs

## Browser Support

Last 2 versions of:
- Chrome
- Firefox
- Safari
- Edge

## Validation Checklist

Before considering a phase complete:
- [ ] CSS validates (W3C)
- [ ] HTML validates (W3C)
- [ ] Focus states visible on all interactive elements
- [ ] Color contrast meets WCAG AA (4.5:1)
- [ ] Works without JavaScript

## Commands Reference

Start a phase:
```
Execute Phase [N] from DEVELOPMENT_ROADMAP.md following SPECIFICATION.md
```

Complete specific tasks:
```
Complete tasks [X.X] through [X.X] from DEVELOPMENT_ROADMAP.md
```

Validate work:
```
Run validation checks for Phase [N]
```

## Important Notes

- The landing page (index.html) must use Purissimo itself (dogfooding)
- All components need documentation with code examples
- This is a portfolio project — quality over speed
- Document the process for the case study

## Do Not

- Add JavaScript to components
- Use CSS frameworks or preprocessors
- Skip accessibility requirements
- Hardcode colors or spacing values
- Forget to update the logs

---

# Using Purissimo with AI

The section below is for AI tools (Claude, ChatGPT, Copilot, etc.) generating HTML with Purissimo.

## How to Include

```html
<link rel="stylesheet" href="purissimo.css">
```

## Component Patterns

### Button

```html
<button class="btn btn--primary">Label</button>
<button class="btn btn--secondary">Label</button>
<button class="btn btn--ghost">Label</button>
<!-- Sizes: btn--sm, btn--lg -->
<!-- Disabled: add disabled attribute -->
```

### Card

```html
<article class="card card--elevated">
  <header class="card__header">
    <h3 class="card__title">Title</h3>
  </header>
  <div class="card__body"><p>Content</p></div>
  <footer class="card__footer">
    <button class="btn btn--primary">Action</button>
  </footer>
</article>
<!-- Variants: card (default), card--elevated, card--outlined, card--glass -->
```

### Form

```html
<div class="form-field">
  <label for="name" class="form-label">Name</label>
  <input type="text" id="name" class="form-input" placeholder="Enter name">
  <span class="form-hint">Helper text.</span>
</div>

<div class="form-field">
  <label for="msg" class="form-label">Message</label>
  <textarea id="msg" class="form-textarea" rows="4"></textarea>
</div>

<div class="form-field">
  <label for="country" class="form-label">Country</label>
  <select id="country" class="form-select">
    <option value="">Select...</option>
  </select>
</div>
```

### Checkbox / Radio / Toggle

```html
<label class="form-checkbox">
  <input type="checkbox">
  <span class="form-checkbox__indicator"></span>
  <span class="form-checkbox__label">Label</span>
</label>

<label class="form-radio">
  <input type="radio" name="group" value="1">
  <span class="form-radio__indicator"></span>
  <span class="form-radio__label">Option</span>
</label>

<label class="form-toggle">
  <input type="checkbox">
  <span class="form-toggle__track"></span>
  <span class="form-toggle__label">Toggle</span>
</label>
```

### Icon

```html
<span class="icon" aria-hidden="true">info</span>
<!-- Available: info, check_circle, warning, error, close -->
```

### Alert

```html
<div class="alert alert--info" role="alert">
  <span class="alert__icon icon" aria-hidden="true">info</span>
  <p class="alert__message">Message text.</p>
</div>
<!-- Icons: info, check_circle (success), warning, error -->
<!-- Variants: alert--info, alert--success, alert--warning, alert--error -->
```

### Accordion

```html
<div class="accordion">
  <details class="accordion__item">
    <summary class="accordion__header">Title</summary>
    <div class="accordion__content"><p>Content</p></div>
  </details>
</div>
```

### Tabs

```html
<div class="tabs">
  <input type="radio" name="tabs" id="tab1" class="tabs__input" checked>
  <label for="tab1" class="tabs__label">Tab 1</label>
  <input type="radio" name="tabs" id="tab2" class="tabs__input">
  <label for="tab2" class="tabs__label">Tab 2</label>
  <div class="tabs__panels">
    <div class="tabs__panel">Content 1</div>
    <div class="tabs__panel">Content 2</div>
  </div>
</div>
```

### Modal

```html
<a href="#my-modal" class="btn btn--primary">Open</a>
<div id="my-modal" class="modal">
  <a href="#" class="modal__overlay" aria-hidden="true"></a>
  <div class="modal__content" role="dialog" aria-modal="true">
    <header class="modal__header">
      <h2 class="modal__title">Title</h2>
      <a href="#" class="modal__close" aria-label="Close"><span class="icon" aria-hidden="true">close</span></a>
    </header>
    <div class="modal__body"><p>Content</p></div>
    <footer class="modal__footer">
      <a href="#" class="btn btn--secondary">Cancel</a>
      <button class="btn btn--primary">Confirm</button>
    </footer>
  </div>
</div>
```

### Navbar

```html
<nav class="navbar container" aria-label="Main navigation">
  <a href="/" class="navbar__brand">Brand</a>
  <ul class="navbar__menu">
    <li><a href="#" class="navbar__link" aria-current="page">Home</a></li>
    <li><a href="#" class="navbar__link">About</a></li>
  </ul>
</nav>
```

### Breadcrumb

```html
<nav class="breadcrumb" aria-label="Breadcrumb">
  <ol>
    <li><a href="/">Home</a></li>
    <li><a href="/docs">Docs</a></li>
    <li aria-current="page">Current</li>
  </ol>
</nav>
```

### Table

```html
<table class="table table--striped">
  <thead><tr><th>Name</th><th>Value</th></tr></thead>
  <tbody><tr><td>Data</td><td>Value</td></tr></tbody>
</table>
```

### Other

```html
<span class="badge badge--primary">Label</span>
<hr class="divider">
<code class="code">inline code</code>
<pre class="code-block"><code>code block</code></pre>
<blockquote class="blockquote"><p>"Quote"</p></blockquote>
```

## Layout

```html
<div class="container">              <!-- max-width: 1200px, centered -->
<div class="container--narrow">      <!-- max-width: 800px -->
<div class="grid gap-4">             <!-- 12-column grid -->
  <div class="col-6 md:col-4">...</div>
</div>
```

## Do's

- Use semantic HTML elements (`<article>`, `<nav>`, `<main>`, `<section>`)
- Include `aria-label` on `<nav>` elements
- Include `role="alert"` on alert components
- Include `role="dialog"` and `aria-modal="true"` on modals
- Use `aria-current="page"` on active navigation links
- Use CSS custom properties for customization
- Always include a skip link: `<a href="#main" class="skip-link">Skip to main content</a>`

## Don'ts

- Don't add JavaScript for component behavior
- Don't use inline styles for colors or spacing (use utility classes or tokens)
- Don't skip the `form-checkbox__indicator` / `form-radio__indicator` spans
- Don't nest components incorrectly (e.g., card inside card)
