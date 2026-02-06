# Purissimo Design System — Specification

> **"Less is pure"**

---

## 1. Overview

**Purissimo** (from Italian "purest") is a minimalist design system built with pure HTML5 and CSS — zero JavaScript in components. It embodies the philosophy that the web, at its core, is already powerful enough.

### Key Facts

- **Author:** Rafael Craice
- **Type:** Personal project / Portfolio piece
- **License:** MIT (suggested)
- **Hosting:** GitHub Pages
- **Repository:** GitHub (public)

### What Makes Purissimo Unique

1. **Pure by design** — HTML5 + CSS only, no JavaScript dependencies
2. **AI-native workflow** — Created in collaboration with AI, optimized for AI usage
3. **Antarctic aesthetic** — Inspired by the purest water on Earth: Antarctic ice
4. **Accessibility-first** — WCAG compliance as a core principle, not an afterthought

---

## 2. Philosophy & Principles

### Manifesto

The modern web is drowning in complexity. Megabytes of JavaScript for a button. Build tools for build tools. Dependencies upon dependencies.

Purissimo is a return to essence.

We believe:
- **The web platform is enough.** HTML and CSS have evolved. We should use them.
- **Simplicity is sustainable.** Less code means less energy, faster loads, longer lifespan.
- **Accessibility is not optional.** If it doesn't work for everyone, it doesn't work.
- **AI is a design partner.** The future of creation is collaborative — human vision, AI execution.

### Core Principles

| Principle | Description |
|-----------|-------------|
| **Purity** | No JavaScript in components. If it can be done with HTML/CSS, it will be. |
| **Clarity** | Clean visual language. Every element has purpose. Nothing decorative without function. |
| **Lightness** | Minimal footprint. Fast loading. Low energy consumption. |
| **Accessibility** | WCAG 2.1 AA compliance minimum. Respects user preferences. |
| **Transparency** | Open process. Documented decisions. Visible tokens. |
| **AI-Friendly** | Consistent patterns that AI tools can understand and generate correctly. |

---

## 3. Design Tokens

### 3.1 Color Palette

Inspired by Antarctic ice — whites, pale blues, subtle grays, with hints of glacial turquoise.

```css
:root {
  /* Base */
  --pure-white: #FFFFFF;
  --ice-white: #F8FAFB;
  --frost: #EEF3F6;
  --mist: #E1E8ED;
  
  /* Grays (cool-toned) */
  --gray-100: #D4DCE2;
  --gray-200: #B8C4CC;
  --gray-300: #9AA8B2;
  --gray-400: #7A8A96;
  --gray-500: #5C6B76;
  --gray-600: #465058;
  --gray-700: #323A40;
  --gray-800: #1F252A;
  --gray-900: #0F1214;
  
  /* Accent (glacial) */
  --glacial-50: #F0F9FA;
  --glacial-100: #D6F0F2;
  --glacial-200: #B0E2E8;
  --glacial-300: #7ACDD6;
  --glacial-400: #4AB5C2;
  --glacial-500: #2E9CAA;
  --glacial-600: #257D8A;
  --glacial-700: #1E6370;
  --glacial-800: #184F5A;
  --glacial-900: #123E47;
  
  /* Semantic */
  --color-text-primary: var(--gray-800);
  --color-text-secondary: var(--gray-500);
  --color-text-muted: var(--gray-400);
  --color-text-inverse: var(--pure-white);
  
  --color-bg-primary: var(--pure-white);
  --color-bg-secondary: var(--ice-white);
  --color-bg-tertiary: var(--frost);
  
  --color-border: var(--mist);
  --color-border-light: var(--frost);
  
  --color-action: var(--glacial-500);
  --color-action-hover: var(--glacial-600);
  --color-action-active: var(--glacial-700);
  
  --color-success: #34A86C;
  --color-warning: #D4A520;
  --color-error: #D64545;
  --color-info: var(--glacial-500);
  
  /* Transparencies */
  --alpha-light: rgba(255, 255, 255, 0.8);
  --alpha-overlay: rgba(15, 18, 20, 0.5);
  --alpha-frost: rgba(238, 243, 246, 0.6);
}
```

### 3.2 Typography

**Font Family:** Outfit (Google Fonts)

```css
:root {
  /* Font Family */
  --font-family-base: 'Outfit', -apple-system, BlinkMacSystemFont, sans-serif;
  --font-family-mono: 'JetBrains Mono', 'Fira Code', monospace;
  
  /* Font Weights */
  --font-weight-light: 300;
  --font-weight-regular: 400;
  --font-weight-medium: 500;
  --font-weight-semibold: 600;
  --font-weight-bold: 700;
  
  /* Font Sizes (base 16px) */
  --font-size-xs: 0.75rem;    /* 12px */
  --font-size-sm: 0.875rem;   /* 14px */
  --font-size-base: 1rem;     /* 16px */
  --font-size-lg: 1.125rem;   /* 18px */
  --font-size-xl: 1.25rem;    /* 20px */
  --font-size-2xl: 1.5rem;    /* 24px */
  --font-size-3xl: 2rem;      /* 32px */
  --font-size-4xl: 2.5rem;    /* 40px */
  --font-size-5xl: 3rem;      /* 48px */
  
  /* Line Heights */
  --line-height-tight: 1.2;
  --line-height-base: 1.5;
  --line-height-relaxed: 1.75;
  
  /* Letter Spacing */
  --letter-spacing-tight: -0.02em;
  --letter-spacing-normal: 0;
  --letter-spacing-wide: 0.02em;
}
```

### 3.3 Spacing

Base-4 grid system.

```css
:root {
  --space-0: 0;
  --space-1: 0.25rem;   /* 4px */
  --space-2: 0.5rem;    /* 8px */
  --space-3: 0.75rem;   /* 12px */
  --space-4: 1rem;      /* 16px */
  --space-5: 1.25rem;   /* 20px */
  --space-6: 1.5rem;    /* 24px */
  --space-8: 2rem;      /* 32px */
  --space-10: 2.5rem;   /* 40px */
  --space-12: 3rem;     /* 48px */
  --space-16: 4rem;     /* 64px */
  --space-20: 5rem;     /* 80px */
  --space-24: 6rem;     /* 96px */
}
```

### 3.4 Borders & Radius

```css
:root {
  /* Border Width */
  --border-width-thin: 1px;
  --border-width-base: 1.5px;
  --border-width-thick: 2px;
  
  /* Border Radius */
  --radius-none: 0;
  --radius-sm: 0.25rem;   /* 4px */
  --radius-base: 0.5rem;  /* 8px */
  --radius-lg: 0.75rem;   /* 12px */
  --radius-xl: 1rem;      /* 16px */
  --radius-full: 9999px;
}
```

### 3.5 Shadows

Subtle, cool-toned shadows for depth without heaviness.

```css
:root {
  --shadow-sm: 0 1px 2px rgba(15, 18, 20, 0.04);
  --shadow-base: 0 2px 8px rgba(15, 18, 20, 0.06);
  --shadow-md: 0 4px 16px rgba(15, 18, 20, 0.08);
  --shadow-lg: 0 8px 32px rgba(15, 18, 20, 0.1);
  --shadow-xl: 0 16px 48px rgba(15, 18, 20, 0.12);
}
```

### 3.6 Transitions

```css
:root {
  --transition-fast: 150ms ease;
  --transition-base: 250ms ease;
  --transition-slow: 400ms ease;
}
```

---

## 4. Grid & Layout

### Container

```css
.container {
  width: 100%;
  max-width: 1200px;
  margin-inline: auto;
  padding-inline: var(--space-4);
}

.container--narrow { max-width: 800px; }
.container--wide { max-width: 1400px; }
```

### Grid System

12-column grid based on CSS Grid.

```css
.grid {
  display: grid;
  gap: var(--space-4);
  grid-template-columns: repeat(12, 1fr);
}

/* Column spans */
.col-1 { grid-column: span 1; }
.col-2 { grid-column: span 2; }
/* ... up to col-12 */

/* Responsive: sm (640px), md (768px), lg (1024px), xl (1280px) */
```

---

## 5. Components

### 5.1 Typography Components

#### Headings

```html
<h1 class="heading-1">Heading 1</h1>
<h2 class="heading-2">Heading 2</h2>
<h3 class="heading-3">Heading 3</h3>
<h4 class="heading-4">Heading 4</h4>
<h5 class="heading-5">Heading 5</h5>
<h6 class="heading-6">Heading 6</h6>
```

#### Body Text

```html
<p class="text-lg">Large body text</p>
<p>Default body text</p>
<p class="text-sm">Small body text</p>
<p class="text-xs">Extra small text</p>
```

#### Text Utilities

```html
<p class="text-muted">Muted text</p>
<p class="text-center">Centered text</p>
<strong class="font-semibold">Semibold text</strong>
```

### 5.2 Buttons

```html
<!-- Primary -->
<button class="btn btn--primary">Primary Action</button>

<!-- Secondary -->
<button class="btn btn--secondary">Secondary Action</button>

<!-- Ghost -->
<button class="btn btn--ghost">Ghost Action</button>

<!-- Sizes -->
<button class="btn btn--primary btn--sm">Small</button>
<button class="btn btn--primary btn--lg">Large</button>

<!-- States (CSS handles :hover, :focus, :active, :disabled) -->
<button class="btn btn--primary" disabled>Disabled</button>
```

### 5.3 Links

```html
<a href="#" class="link">Default link</a>
<a href="#" class="link link--subtle">Subtle link</a>
<a href="#" class="link link--nav">Navigation link</a>
```

### 5.4 Forms

#### Text Input

```html
<div class="form-field">
  <label for="name" class="form-label">Name</label>
  <input type="text" id="name" class="form-input" placeholder="Enter your name">
  <span class="form-hint">Your full name as it appears on documents.</span>
</div>

<!-- With validation states (CSS :valid, :invalid) -->
<input type="email" class="form-input" required>
```

#### Textarea

```html
<div class="form-field">
  <label for="message" class="form-label">Message</label>
  <textarea id="message" class="form-textarea" rows="4"></textarea>
</div>
```

#### Select

```html
<div class="form-field">
  <label for="country" class="form-label">Country</label>
  <select id="country" class="form-select">
    <option value="">Select a country</option>
    <option value="br">Brazil</option>
    <option value="us">United States</option>
  </select>
</div>
```

#### Checkbox

```html
<label class="form-checkbox">
  <input type="checkbox">
  <span class="form-checkbox__indicator"></span>
  <span class="form-checkbox__label">I agree to the terms</span>
</label>
```

#### Radio

```html
<fieldset class="form-fieldset">
  <legend class="form-legend">Select an option</legend>
  <label class="form-radio">
    <input type="radio" name="option" value="1">
    <span class="form-radio__indicator"></span>
    <span class="form-radio__label">Option 1</span>
  </label>
  <label class="form-radio">
    <input type="radio" name="option" value="2">
    <span class="form-radio__indicator"></span>
    <span class="form-radio__label">Option 2</span>
  </label>
</fieldset>
```

#### Toggle/Switch

```html
<label class="form-toggle">
  <input type="checkbox">
  <span class="form-toggle__track"></span>
  <span class="form-toggle__label">Enable notifications</span>
</label>
```

### 5.5 Tables

```html
<table class="table">
  <thead>
    <tr>
      <th>Name</th>
      <th>Email</th>
      <th>Role</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John Doe</td>
      <td>john@example.com</td>
      <td>Designer</td>
    </tr>
  </tbody>
</table>

<!-- Variants -->
<table class="table table--striped">...</table>
<table class="table table--bordered">...</table>
```

### 5.6 Cards

```html
<article class="card">
  <header class="card__header">
    <h3 class="card__title">Card Title</h3>
  </header>
  <div class="card__body">
    <p>Card content goes here.</p>
  </div>
  <footer class="card__footer">
    <button class="btn btn--primary">Action</button>
  </footer>
</article>

<!-- Variants -->
<article class="card card--elevated">...</article>
<article class="card card--outlined">...</article>
<article class="card card--glass">...</article> <!-- Frosted glass effect -->
```

### 5.7 Icons (Material Symbols)

Purissimo uses Google Material Symbols Outlined for iconography. Only a subset of icons is loaded via the `icon_names` parameter for performance (~2KB vs 295KB full set).

```html
<!-- Basic usage -->
<span class="icon" aria-hidden="true">info</span>

<!-- Available ligatures -->
<!-- info, check_circle, warning, error, close -->
```

The `.icon` class sets the font family, size (`1.25rem`), and rendering properties. Use `aria-hidden="true"` since icons are decorative — the meaning is conveyed by surrounding text or `aria-label`.

### 5.8 Alerts / Messages

```html
<div class="alert alert--info" role="alert">
  <span class="alert__icon icon" aria-hidden="true">info</span>
  <p class="alert__message">This is an informational message.</p>
</div>

<div class="alert alert--success" role="alert">...</div>
<div class="alert alert--warning" role="alert">...</div>
<div class="alert alert--error" role="alert">...</div>
```

### 5.9 Navigation

#### Nav Bar

```html
<nav class="navbar" aria-label="Main navigation">
  <a href="/" class="navbar__brand">Purissimo</a>
  <ul class="navbar__menu">
    <li><a href="#" class="navbar__link">Home</a></li>
    <li><a href="#" class="navbar__link" aria-current="page">Docs</a></li>
    <li><a href="#" class="navbar__link">About</a></li>
  </ul>
</nav>
```

#### Breadcrumb

```html
<nav class="breadcrumb" aria-label="Breadcrumb">
  <ol>
    <li><a href="/">Home</a></li>
    <li><a href="/docs">Documentation</a></li>
    <li aria-current="page">Components</li>
  </ol>
</nav>
```

### 5.10 Interactive Components (No JS)

#### Accordion

```html
<div class="accordion">
  <details class="accordion__item">
    <summary class="accordion__header">Section 1</summary>
    <div class="accordion__content">
      <p>Content for section 1.</p>
    </div>
  </details>
  <details class="accordion__item">
    <summary class="accordion__header">Section 2</summary>
    <div class="accordion__content">
      <p>Content for section 2.</p>
    </div>
  </details>
</div>
```

#### Tabs (using radio buttons)

```html
<div class="tabs">
  <input type="radio" name="tabs" id="tab1" class="tabs__input" checked>
  <label for="tab1" class="tabs__label">Tab 1</label>
  
  <input type="radio" name="tabs" id="tab2" class="tabs__input">
  <label for="tab2" class="tabs__label">Tab 2</label>
  
  <input type="radio" name="tabs" id="tab3" class="tabs__input">
  <label for="tab3" class="tabs__label">Tab 3</label>
  
  <div class="tabs__panels">
    <div class="tabs__panel" data-panel="tab1">Content 1</div>
    <div class="tabs__panel" data-panel="tab2">Content 2</div>
    <div class="tabs__panel" data-panel="tab3">Content 3</div>
  </div>
</div>
```

#### Modal (using :target)

```html
<a href="#modal-example" class="btn btn--primary">Open Modal</a>

<div id="modal-example" class="modal">
  <div class="modal__overlay"></div>
  <div class="modal__content" role="dialog" aria-modal="true">
    <header class="modal__header">
      <h2 class="modal__title">Modal Title</h2>
      <a href="#" class="modal__close" aria-label="Close modal"><span class="icon" aria-hidden="true">close</span></a>
    </header>
    <div class="modal__body">
      <p>Modal content here.</p>
    </div>
    <footer class="modal__footer">
      <a href="#" class="btn btn--secondary">Cancel</a>
      <button class="btn btn--primary">Confirm</button>
    </footer>
  </div>
</div>
```

#### Tooltip

```html
<span class="tooltip">
  Hover me
  <span class="tooltip__content">Tooltip text</span>
</span>

<!-- Or with focus support -->
<button class="tooltip" aria-describedby="tip1">
  Info
  <span class="tooltip__content" role="tooltip" id="tip1">More information here</span>
</button>
```

### 5.11 Lists

```html
<ul class="list">
  <li>Item 1</li>
  <li>Item 2</li>
</ul>

<ol class="list list--ordered">
  <li>First</li>
  <li>Second</li>
</ol>

<ul class="list list--none">
  <li>No bullets</li>
</ul>
```

### 5.12 Badges / Tags

```html
<span class="badge">Default</span>
<span class="badge badge--primary">Primary</span>
<span class="badge badge--success">Success</span>
<span class="badge badge--warning">Warning</span>
<span class="badge badge--error">Error</span>
```

### 5.13 Dividers

```html
<hr class="divider">
<hr class="divider divider--subtle">
```

### 5.14 Code

```html
<code class="code">inline code</code>

<pre class="code-block"><code>
function hello() {
  console.log("Hello, Purissimo!");
}
</code></pre>
```

### 5.15 Blockquote

```html
<blockquote class="blockquote">
  <p>"Less is pure."</p>
  <footer class="blockquote__footer">
    <cite>Purissimo</cite>
  </footer>
</blockquote>
```

### 5.16 Image

```html
<figure class="figure">
  <img src="image.jpg" alt="Description" class="figure__image">
  <figcaption class="figure__caption">Image caption</figcaption>
</figure>
```

---

## 6. Accessibility

### Requirements

- **WCAG 2.1 Level AA** compliance minimum
- All interactive elements keyboard accessible
- Visible focus states
- Sufficient color contrast (4.5:1 for text, 3:1 for large text)
- Screen reader compatible (proper ARIA labels, roles, semantic HTML)

### User Preference Support

```css
/* Reduced motion */
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}

/* High contrast */
@media (prefers-contrast: more) {
  :root {
    --color-border: var(--gray-500);
    --shadow-base: none;
  }
}
```

### Focus States

All interactive elements must have visible focus indicators:

```css
:focus-visible {
  outline: 2px solid var(--color-action);
  outline-offset: 2px;
}
```

### Documentation Requirement

Each component must document:
- WCAG success criteria met
- Required ARIA attributes
- Keyboard interaction pattern

---

## 7. Browser Support

Support for the last 2 versions of major browsers:
- Chrome
- Firefox
- Safari
- Edge

Modern CSS features allowed:
- CSS Custom Properties (variables)
- CSS Grid
- Flexbox
- `:has()` selector
- `:focus-visible`
- `@container` queries (for advanced use)
- `@layer` (for cascade organization)

---

## 8. Project Structure

```
purissimo/
├── purissimo.css           # Main CSS file (single file distribution)
├── purissimo.min.css       # Minified production version
├── index.html              # Landing page + Documentation
├── catalog.html            # Component catalog / storybook
├── examples.html           # Component composition recipes
├── AI.md                   # AI usage instructions
├── SPECIFICATION.md        # This file
├── README.md               # Project readme
├── LICENSE                 # MIT License
└── examples/
    └── template.html       # Starter template for new projects
```

---

## 9. Landing Page Structure

### Sections

1. **Hero**
   - Logo/Name: Purissimo
   - Tagline: "Less is pure"
   - Brief description
   - CTA: View Documentation / Get Started

2. **Manifesto**
   - The philosophy behind Purissimo
   - Why pure HTML/CSS matters
   - The three pillars: Simplicity, Accessibility, Sustainability

3. **Principles**
   - Visual cards or list explaining core principles
   - Icons or illustrations for each

4. **Component Showcase**
   - Interactive preview of all components
   - Live examples using the design system itself
   - Code snippets for each

5. **Design Tokens**
   - Visual display of colors, typography, spacing
   - Copyable CSS variables

6. **The Process**
   - Case study: How Purissimo was created
   - The AI collaboration story
   - Key design decisions with rationale
   - Screenshots/excerpts of the conversation

7. **How to Use**
   - Installation (CDN, download, npm)
   - Basic usage example
   - Link to CLAUDE.md for AI users

8. **Metrics**
   - Lighthouse scores
   - WCAG compliance level
   - File size comparison with other systems

9. **Roadmap**
   - Version 1.0 features
   - Future plans (v2, v3...)

10. **About**
    - About Rafael Craice
    - Links (portfolio, LinkedIn, GitHub)

11. **Footer**
    - License info
    - GitHub link
    - "Made with AI, designed for humans"

---

## 10. Documentation Requirements

### For Each Component

1. **Preview** — Visual example
2. **Description** — What it is, when to use it
3. **Code** — HTML markup (copyable)
4. **Variants** — All available variations
5. **States** — Hover, focus, active, disabled
6. **Accessibility** — WCAG criteria, ARIA requirements, keyboard support
7. **Do's and Don'ts** — Usage guidelines

### Design Decisions Section

Document the "why" behind major decisions:
- Why base-4 spacing?
- Why Outfit font?
- Why no JavaScript?
- Why this color palette?
- Why these specific components?

---

## 11. CLAUDE.md Content

Instructions for AI tools to correctly use Purissimo:

```markdown
# Using Purissimo with AI

## Overview
Purissimo is a pure HTML5/CSS design system. No JavaScript required.

## How to Include
​```html
<link rel="stylesheet" href="purissimo.css">
​```

## Naming Conventions
- Components: `.component-name` (kebab-case)
- Variants: `.component-name--variant`
- Children: `.component-name__child`
- Utilities: `.utility-name`

## Component Patterns
[Include canonical HTML structure for each component]

## Do's
- Use semantic HTML elements
- Include proper ARIA labels
- Follow the documented structure exactly
- Use CSS variables for customization

## Don'ts
- Don't add JavaScript for component behavior
- Don't modify the class naming convention
- Don't use inline styles
- Don't nest components incorrectly

## Examples
[Include complete page examples]
```

---

## 12. Metrics & Validation

### To Measure

1. **Performance**
   - Lighthouse Performance score (target: 95+)
   - Total CSS file size (target: <50KB minified)
   - Time to First Paint

2. **Accessibility**
   - Lighthouse Accessibility score (target: 100)
   - axe-core audit (0 violations)
   - WCAG 2.1 AA compliance (document each criterion)

3. **Comparison**
   - File size vs Bootstrap, Tailwind, etc.
   - Feature comparison table

### Validation Tools
- W3C CSS Validator
- W3C HTML Validator
- axe DevTools
- Lighthouse
- WAVE

---

## 13. Roadmap

### Version 1.0 (Initial Release)
- All base components
- Landing page with documentation
- CLAUDE.md for AI usage
- Lighthouse score 95+
- WCAG 2.1 AA compliance

### Version 1.1 (Current)
- Material Symbols Outlined icon system (`.icon` class with subseted font)
- Component catalog page (`catalog.html`)
- Component recipes / examples page (`examples.html`)
- Alert icons migrated from emoji to Material Symbols
- Modal close button migrated to Material Symbols

### Version 2.0 (Future)
- Dark mode (optional, user preference)
- Additional themes
- Component playground
- Figma design kit

---

## 14. Process Documentation

### The Story

This design system was created through a collaborative process between a human product designer (Rafael Craice) and an AI assistant (Claude). The process itself is part of the case study.

### Key Moments to Document

1. **Initial Brief** — The original request and constraints
2. **Discovery Questions** — How the AI asked clarifying questions to understand scope
3. **Design Decisions** — Each major decision with rationale
4. **Iteration** — How requirements evolved through conversation
5. **Technical Choices** — Why specific CSS approaches were chosen
6. **Reflection** — What worked, what was challenging

### The AI-Driven Design Angle

This project demonstrates:
- How designers can use AI as a thinking partner
- How clear requirements lead to better AI output
- The value of iterative refinement in AI collaboration
- A new workflow for design system creation

---

## 15. Implementation Notes

### CSS Organization

Use `@layer` for cascade organization:

```css
@layer reset, tokens, base, components, utilities;

@layer reset {
  /* CSS reset */
}

@layer tokens {
  :root { /* all variables */ }
}

@layer base {
  /* Base element styles */
}

@layer components {
  /* All components */
}

@layer utilities {
  /* Utility classes */
}
```

### File Header

```css
/*!
 * Purissimo Design System
 * "Less is pure"
 * 
 * Version: 1.1.0
 * Author: Rafael Craice
 * License: MIT
 * Repository: https://github.com/[username]/purissimo
 * 
 * A pure HTML5/CSS design system inspired by Antarctic ice.
 * Zero JavaScript. Maximum accessibility.
 * Created in collaboration with AI, optimized for AI.
 */
```

---

## Appendix: Design Decision Log

| Decision | Choice | Rationale |
|----------|--------|-----------|
| Base spacing | 4px | Industry standard, works well with common font sizes |
| Font | Outfit | Geometric sans-serif, delicate, modern, excellent readability |
| Color inspiration | Antarctic ice | Represents purity, clarity, and the "purest water" concept |
| No JavaScript | Principle | Demonstrates HTML/CSS capability, improves accessibility and performance |
| Single CSS file | Simplicity | Easy distribution, no build step required |
| WCAG AA | Minimum standard | Balances accessibility with design flexibility |
| AI-friendly docs | Future-proof | Design systems will increasingly be used by AI tools |

---

*This specification was created through human-AI collaboration, documenting the entire discovery and decision-making process.*
