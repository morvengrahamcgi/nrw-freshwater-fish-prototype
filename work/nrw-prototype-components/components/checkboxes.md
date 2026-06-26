# Checkboxes

## Source

- Figma export: `Building blocks/Checkboxes/Input`
- Figma export: `Building blocks/Checkboxes/Item`
- GOV.UK baseline: use GOV.UK checkbox semantics and behaviour for one or more selections.

## Purpose

Use checkboxes when users can select more than one option, or when they need to confirm a single statement.

## Medium Default Layout

- Checkbox item width: `640px`.
- Default item height without hint: `40px`.
- Input row: horizontal flex row, align start, gap `16px`.
- Checkbox input: `40px` by `40px`.
- Default border: `2px solid #1F1F1F`.
- Focus border: `4px solid #1F1F1F`.
- Medium focus ring: `0 0 0 3px #FFDD00`.
- Selected icon: `25px` by `20px`, `#1F1F1F`.
- Content column: flex column, justify centre, padding `4px 0`, gap `5px`.
- Content column width: `584px`.

## Typography

- Label: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Hint: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Component labels and hints should not be bold.

## Small Variant

- Checkbox input: `32px` by `32px`.
- Small focus ring: `0 0 0 6px #FFDD00`.
- Selected icon: `17.5px` by `14px`, `#1F1F1F`.
- Label: Gotham Rounded Book, `14px`, `24px` line height, `#333333`.

## Disabled State

- Disabled border: `2px solid #E3E3E3`.
- Disabled selected icon: `#E3E3E3`.

## Reveal Variant

- Reveal panel: `630px` wide, `75px` high, padding `0 0 0 18px`, gap `34px`.
- Reveal left border: `4px` wide, `#B1B4B6`.
- Nested text input area: `574px` wide, `75px` high.

## Prototype Notes

- Use `.nrw-checkboxes`, `.nrw-checkbox-item`, `.nrw-checkbox-control`, `.nrw-checkbox-content`, `.nrw-checkbox-label`, `.nrw-checkbox-hint`, and `.nrw-checkbox-reveal` from `styles/nrw.css`.
- Add `.nrw-checkboxes--small` for the small variant.
- Keep the native checkbox input in the markup for accessibility, then visually style the adjacent `.nrw-checkbox-control`.
- Use `fieldset` and `legend` around grouped checkboxes.
