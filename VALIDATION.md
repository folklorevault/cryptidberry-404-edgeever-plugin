# Validation report

Validated on 2026-10-10 against the current public EdgeEver source and plugin-development documentation.

## Package checks

- The manifest passes EdgeEver's own `parseExtensionManifest` parser as a plugin with API version 2.
- The package targets `web` and `desktop` and declares zero permissions.
- `main.js` passes Node's module syntax check. It only returns an empty deactivation function.
- `manifest.json`, `palette.json`, `main.js`, and `styles.css` pass Prettier's parser and formatting check.
- The design detector reports no unresolved findings. Two preview-only exceptions are recorded: pane children intentionally meet EdgeEver's structural dividers, and the cream surfaces are the requested sourced Moon Milk/Welborn paper colors.

## Contrast checks

Representative text pairs were checked using the WCAG relative-luminance formula. Ratios are listed as foreground on background.

### Light mode

| Pair                                               |   Ratio |
| -------------------------------------------------- | ------: |
| Shadow Grape `#180E2D` on Welborn Paper `#F4EFE3`  | 16.06:1 |
| Muted text `#4E584A` on Welborn Paper `#F4EFE3`    |  6.49:1 |
| Muted text `#4E584A` on pale berry `#E4D9DF`       |  5.42:1 |
| Mist Lavender `#7A5BB8` on Welborn Paper `#F4EFE3` |  4.56:1 |
| Electric Pear `#A6B72F` on Shadow Grape `#180E2D`  |  8.28:1 |
| Oxblood `#6E1F2A` on Welborn Paper `#F4EFE3`       |  9.67:1 |
| Success `#52620F` on Welborn Paper `#F4EFE3`       |  5.88:1 |
| Warning `#865A20` on Welborn Paper `#F4EFE3`       |  5.23:1 |

### Dark mode

| Pair                                              |   Ratio |
| ------------------------------------------------- | ------: |
| Moon Milk `#EFE7DA` on Shadow Grape `#180E2D`     | 15.02:1 |
| Ghostberry `#C6A4BE` on Shadow Grape `#180E2D`    |  8.30:1 |
| Ghostberry `#C6A4BE` on deep berry `#2B1535`      |  7.50:1 |
| Electric Pear `#A6B72F` on Indigo Night `#040613` |  9.07:1 |
| Dusky Blush `#D08095` on Shadow Grape `#180E2D`   |  6.32:1 |
| Warning `#D6A45B` on Shadow Grape `#180E2D`       |  8.18:1 |

Mist Lavender on Indigo Night measures 3.52:1 and is reserved for non-text boundaries in dark mode.

## Visual review status

The selectors and visual roles were reviewed against the supplied EdgeEver light and dark screenshots and the current public source. A static three-pane preview was also inspected at source level. The package has not yet been installed in a live EdgeEver client, so the final light/dark acceptance pass remains to be done after publication and installation.
