# .ionity-assets

> Public brand and design assets for **[ionity.today](https://ionity.today)** — Ionity Global (Pty) Ltd and related properties.

---

## Contents

| Path | Description |
|------|-------------|
| [`logos/`](./logos/) | Primary, light, and dark variants of the Ionity wordmark logo (SVG) |
| [`icons/`](./icons/) | App icon and favicon (SVG) |
| [`colors/`](./colors/) | Color palette as JSON tokens and CSS custom properties |
| [`fonts/`](./fonts/) | Font references and licensing notes |
| [`images/`](./images/) | Open Graph images, banners, and backgrounds |
| [`manifest.json`](./manifest.json) | Machine-readable index of all available assets |
| [`metadata.json`](./metadata.json) | Brand and organisation metadata |

---

## Quick Start

### Logos

| File | Usage |
|------|-------|
| `logos/ionity-logo-primary.svg` | Use on white or light backgrounds (default) |
| `logos/ionity-logo-light.svg` | Use on dark or colored backgrounds |
| `logos/ionity-logo-dark.svg` | Dark wordmark for light backgrounds |

### Colors

**CSS** — import the stylesheet and use the custom properties:

```html
<link rel="stylesheet" href="colors/ionity-colors.css">
```

```css
.button {
  background-color: var(--ionity-primary);
  color: var(--ionity-background);
}
```

**JSON** — consume the token file in design tools or build pipelines:

```js
import colors from './colors/ionity-colors.json';
console.log(colors.colors.brand.primary.value); // #0A0AFF
```

### Asset Manifest

Use `manifest.json` to programmatically discover all available assets:

```js
import manifest from './manifest.json';
console.log(manifest.assets.logos);
```

### Metadata

Use `metadata.json` for organisation and brand details:

```js
import meta from './metadata.json';
console.log(meta.name);   // Ionity Global (Pty) Ltd
console.log(meta.colors); // { primary: '#0A0AFF', ... }
```

---

## NPM / Package Usage

This repository is published as [`@ionity/assets`](https://www.npmjs.com/package/@ionity/assets).

```bash
npm install @ionity/assets
```

---

## Brand Guidelines

- Always maintain clear space around the logo equal to the height of the "i" letterform.
- Do not recolor the primary logo. Use the light or dark variants for alternate backgrounds.
- Do not stretch, skew, or add effects to any logo or icon.
- For questions or permissions, contact [hello@ionity.today](mailto:hello@ionity.today).

---

## License

[MIT](./LICENSE) © 2024–2026 Ionity Global (Pty) Ltd
