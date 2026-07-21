# Sherpa Component Kit

This is the reusable component/design-system layer for the Sherpa prototype. Devs can copy or import `sherpa-components.css` across projects instead of re-prompting for modal, button, field, and hover-state details.

## What This Is Called

This is a lightweight **component library** or **design system kit**. It includes:

- Design tokens: colors, typefaces, radii, borders, hover states
- Modal shell: overlay, frosted card, glow layer, title/body layout
- Buttons: primary, secondary, disabled, hover states
- Inputs/selects: default, hover, focus, filled states
- Checkbox: custom filled state with aligned tick
- Frosted panels: reusable glassy surface treatment

## How To Use

Add this in the HTML `<head>`:

```html
<link rel="stylesheet" href="./sherpa-components.css">
```

Wrap reusable UI in `.sherpa-ui`:

```html
<div class="sherpa-ui">
  <!-- Sherpa components here -->
</div>
```

## Modal Example

```html
<div class="sherpa-ui sherpa-modal-overlay" role="dialog" aria-modal="true">
  <div class="sherpa-modal">
    <div class="sherpa-stack">
      <div class="sherpa-center-copy">
        <h2 class="sherpa-title">Sherpa needs a bit more context</h2>
        <p class="sherpa-body">
          Keep chatting so Sherpa can learn about you. Or skip for now and use the editor without Sherpa.
        </p>
      </div>

      <div class="sherpa-button-group">
        <button class="sherpa-button sherpa-button-primary" type="button">Keep chatting</button>
        <button class="sherpa-button" type="button">Continue without Sherpa</button>
      </div>
    </div>
  </div>
</div>
```

## Form Example

```html
<form class="sherpa-ui sherpa-form">
  <label class="sherpa-field">
    <span class="sherpa-label">Title</span>
    <input class="sherpa-input" type="text" placeholder="Episode title">
  </label>

  <label class="sherpa-field">
    <span class="sherpa-label">Sub-genre</span>
    <input class="sherpa-input" type="text" placeholder="Supernatural">
  </label>

  <label class="sherpa-checkbox">
    <input type="checkbox">
    <span class="sherpa-checkmark"></span>
    <span class="sherpa-checkbox-text">I confirm I’m the sole copyright owner of this content.</span>
  </label>

  <button class="sherpa-button sherpa-button-primary" type="submit" disabled>Open editor</button>
</form>
```

## Select Example

The CSS provides styling; app code should handle open/close and selected state.

```html
<div class="sherpa-select">
  <button class="sherpa-select-button is-placeholder" type="button">
    <span>Select genre</span>
    <span aria-hidden="true">⌄</span>
  </button>

  <div class="sherpa-select-menu" role="listbox">
    <button class="sherpa-select-option" type="button" role="option">Drama</button>
    <button class="sherpa-select-option" type="button" role="option">Fantasy</button>
    <button class="sherpa-select-option" type="button" role="option">Horror</button>
  </div>
</div>
```

Use these classes for state:

- `.is-open` on `.sherpa-select`
- `.has-value` on `.sherpa-select`
- `.is-active` on `.sherpa-select-option`
- `.is-placeholder` on `.sherpa-select-button`

## Key Tokens

```css
:root {
  --sherpa-border: #2f2f2f;
  --sherpa-surface-hover: rgba(102,102,102,.2);
  --sherpa-surface-disabled: #545454;
  --sherpa-text-disabled: #828282;
  --sherpa-radius-card: 24px;
  --sherpa-radius-field: 12px;
  --sherpa-radius-pill: 60px;
}
```

## GitHub

These files are part of the repo:

- `sherpa-components.css`
- `COMPONENTS.md`

When devs clone or download the repo, they can import `sherpa-components.css` directly into any prototype or app page.
