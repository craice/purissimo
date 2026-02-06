# Purissimo

> **"Less is pure"**

A minimalist design system built with pure HTML5 and CSS — zero JavaScript. Inspired by the purest water on Earth: Antarctic ice.

## Features

- **Pure HTML5 + CSS** — No JavaScript dependencies, ever
- **Accessible** — WCAG 2.1 AA compliant with `prefers-reduced-motion` and `prefers-contrast` support
- **Lightweight** — Single CSS file (~39KB minified), no build tools required
- **Modern CSS** — Custom properties, Grid, Flexbox, `@layer`, logical properties
- **AI-friendly** — Consistent BEM patterns optimized for AI-assisted development
- **Responsive** — Mobile-first with breakpoints at 640px, 768px, 1024px, and 1280px

## Quick Start

1. Download `purissimo.css` (or `purissimo.min.css` for production) and add it to your project:

```html
<link rel="stylesheet" href="purissimo.css">
```

2. Use semantic HTML with Purissimo classes:

```html
<button class="btn btn--primary">Get Started</button>
```

3. Copy the starter template from `examples/template.html` to get going fast.

## What's Included

### Components

Buttons, links, forms (inputs, selects, checkboxes, radios, toggles), cards, alerts, tables, accordion, tabs, modal, tooltip, badges, breadcrumb, navbar, dividers, code blocks, blockquotes, and figures.

### Utilities

Container, 12-column responsive grid, spacing (margin/padding), flexbox, display, text alignment, screen-reader-only, and width utilities.

### Design Tokens

80+ CSS custom properties for colors (Antarctic ice palette), typography (Outfit + JetBrains Mono), spacing (base-4 scale), borders, shadows, and transitions.

## Installation

### Option 1: Direct download

Download `purissimo.css` from this repository and link it in your HTML.

### Option 2: CDN (GitHub Pages)

```html
<link rel="stylesheet" href="https://craice.github.io/purissimo/purissimo.min.css">
```

## File Sizes

| File | Size |
|------|------|
| `purissimo.css` | ~61KB |
| `purissimo.min.css` | ~40KB |

No images. No JavaScript. No external dependencies beyond Google Fonts (Outfit, JetBrains Mono, Material Symbols Outlined).

## Documentation

Visit the [Purissimo documentation](https://craice.github.io/purissimo) for the full component reference, design tokens, and usage guidelines.

## Using with AI

Purissimo is designed to work well with AI coding assistants. The `AI.md` file contains canonical HTML patterns for every component, making it easy for AI tools to generate correct Purissimo markup. Simply include it in your project context.

## Browser Support

Last 2 versions of:

- Chrome
- Firefox
- Safari
- Edge

## Contributing

Purissimo is a personal project, but contributions are welcome:

1. Fork the repository
2. Create a feature branch
3. Make your changes to `purissimo.css`
4. Test across supported browsers
5. Submit a pull request

Please follow the existing BEM naming conventions and use CSS custom properties for all values.

## License

[MIT](LICENSE) — Rafael Craice
