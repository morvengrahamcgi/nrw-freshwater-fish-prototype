# Unit Switch Input

## Source

- Figma export: unit switch text input component supplied on 2026-06-26.
- GOV.UK baseline: use GOV.UK text input semantics, labels, hints, validation, input mode, and error messages.

## Purpose

Use this component where a user enters one numeric value and can switch between two units, such as acres and hectares. Use it instead of radio buttons when one unit should be the default.

## Layout

- Component width: `640px`.
- Component gap: `24px` between the text input group and the switch link.
- Text input group width: `640px`.
- Text input group gap: `4px`.
- Label: Gotham Rounded Bold, `16px`, `24px` line height, `#333333`.
- Input width: `640px`.
- Input height: `48px`.
- Input padding: `12px 16px`.
- Input border: `2px solid #1F1F1F`.
- Input text: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Switch link: Gotham Rounded Bold, `16px`, `24px` line height, `#007485`.

## Prototype Notes

- Use `.nrw-unit-input`, `.nrw-unit-input__field`, `.nrw-unit-input__label`, `.nrw-text-input--unit`, and `.nrw-unit-input__switch`.
- Keep the active unit in the visible label.
- Use a hidden field to preserve the current unit for review pages.
- Default to the most common or preferred unit, then use a link-style button such as `Switch to hectares`.
