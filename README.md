# Cryptidberry 404 for EdgeEver

This is the complete desktop/web treatment: application chrome and rendered note content in one installable EdgeEver plugin package.

## Why this package is a plugin

EdgeEver's declarative theme API is the correct long-term interface and a pure theme version is included separately. In the current EdgeEver source, however, several stock dark-workspace selectors have higher specificity than the public theme selectors. A pure theme can therefore leave parts of the dark three-pane workspace on the stock colors.

This package uses EdgeEver's supported optional `styles.css` plugin asset to cover those surfaces reliably. The required `main.js` is an inert activation stub. The plugin declares no permissions, reads no notes, stores nothing, and makes no network requests.

## Package

- `manifest.json` — EdgeEver plugin metadata; zero permissions; desktop and web only.
- `main.js` — required inert activation/deactivation stub.
- `styles.css` — whole-interface light and dark palette plus scoped ProseMirror content styling.
- `palette.json` — exact source colors kept separate from theme-specific derived colors.
- `VALIDATION.md` — compatibility, syntax, contrast, and visual-review notes.

## Installation model

EdgeEver installs community plugins from a public GitHub repository or public manifest URL.

1. Publish these files at a stable public URL, or place them in a public GitHub repository and create a `v1.0.0` release containing `manifest.json`, `main.js`, and `styles.css`.
2. In EdgeEver's Plugin Marketplace, install the repository URL or manifest URL.
3. Enable **Cryptidberry 404**.
4. Disable the earlier Custom CSS after confirming the plugin is active; this package already contains the editor-content treatment.
5. Check light and dark appearances on the actual Mac/web client.

No repository has been published and no live EdgeEver installation has been changed.

## Compatibility

- EdgeEver web: supported.
- EdgeEver desktop: supported.
- EdgeEver native Android and iOS: plugins do not run there.
- Monaspace Xenon is requested by name. If unavailable, the interface falls back to SF Mono, Menlo, or another monospace font.

## Visual roles

- Cryptidberry supplies the indigo, berry, lavender, blush, Moon Milk, and Ghostberry room.
- Welborn electric pear is the action, selection, checkbox, focus, and search color.
- Oxblood is used for destructive or weight-bearing light-mode roles, rules, and the caret—not as a competing primary action color.
- Dark mode uses Dusky Blush as the accessible danger counterpart to oxblood.
