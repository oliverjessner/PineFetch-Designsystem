# PineFetch Design System

Only 10kb

A small, reusable design system for PineFetch, PineFetch Link Dump, and compact tools such as browser extensions, Tauri mini apps, local admin panels, and internal utilities.

This repo does not contain the full PineFetch app. It only extracts the general UI building blocks from the PineFetch CSS structure.

## Apps

| PineFetch                                                                 | PineFetch Link Dump                                                                           |
| ------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| <img src="assets/images/pinefetch.webp" alt="PineFetch logo" width="120"> | <img src="assets/images/pinefetch-link-dump.webp" alt="PineFetch Link Dump logo" width="120"> |

## Files

- [`design-system/pinefetch.css`](design-system/pinefetch.css): dependency-free CSS, usable directly via `<link>`.
- [`design-system/example.html`](design-system/example.html): standalone example page with all components.
- [`ai-guide.md`](ai-guide.md): guide for AI assistants and code generators.
- [`assets/images/`](assets/images/): logos and image assets for PineFetch projects.

## Quick Start

```html
<link rel="stylesheet" href="design-system/pinefetch.css" />
```

```html
<main class="pf-app-shell pf-app-shell-narrow">
    <section class="pf-panel">
        <header class="pf-panel-header">
            <div class="pf-panel-heading">
                <h1 class="pf-title">Mini Tool</h1>
                <p class="pf-subtitle">Compact PineFetch-style UI.</p>
            </div>
            <span class="pf-badge">Ready</span>
        </header>

        <label class="pf-field">
            <span class="pf-label">URL</span>
            <input class="pf-input" type="url" placeholder="https://..." />
        </label>

        <button class="pf-btn pf-btn-primary" type="button">Run</button>
    </section>
</main>
```

## Components

The CSS provides reusable building blocks:

- Tokens and CSS custom properties with `--pf-`
- Monospace typography and a dark base layout
- Panels, panel headers, and small soft panels
- Buttons, primary buttons, ghost buttons, and danger buttons
- Badges
- Inputs, selects, textareas, labels, and field rows
- Hints, status text, and dividers
- Toggles and segmented controls
- Focus, hover, disabled, active, loading, and invalid states
- Small utility classes such as `pf-stack`, `pf-row`, `pf-grid`, `pf-grow`, `pf-w-full`

All public classes start with `pf-` so the design system does not collide with existing class names in other projects.

## For AI Assistants

When using this design system in a new UI:

- Start with `.pf-app-shell` or `.pf-panel`.
- Use `.pf-app-shell-narrow` for Chrome extension popups.
- Use `.pf-btn pf-btn-primary` for the main action.
- Use `.pf-badge` for short status labels.
- Use `.pf-field`, `.pf-label`, `.pf-input`, `.pf-select`, and `.pf-textarea` for forms.
- Use existing `--pf-` tokens instead of defining custom colors.
- Do not use old PineFetch app IDs such as `#startDownloadBtn`, `#queueList`, `#historyView`, or `#urlInput`.
- Do not use unprefixed classes such as `.btn`, `.badge`, `.panel`, or `.field`.

Details are available in [`ai-guide.md`](ai-guide.md).

## View the Example

The example page can be opened directly in the browser:

```txt
design-system/example.html
```

It shows a panel, header, badge, input, select, textarea, primary/ghost/danger buttons, toggle, segmented control, hint, and status text.
