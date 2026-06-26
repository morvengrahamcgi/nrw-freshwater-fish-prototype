# Radios

## Source

- Figma export: `Building blocks/Radios/Item`
- Figma export: `Form Elements / Radio Button`
- GOV.UK baseline: use GOV.UK radio semantics and behaviour for grouped single-choice questions.

## Purpose

Use radios when users must choose one option from a list.

## Medium Default Layout

- Full radio group width: `640px`.
- Group layout: vertical flex column, gap `16px`.
- Group label and hint block width: `630px`, gap `4px`.
- Group label: Gotham Rounded Bold, `18px`, `24px` line height, `#333333`.
- Group hint: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Radio buttons list: vertical flex column, gap `24px`.
- Component examples sit in a `640px` content width.
- Radio option wrapper layout: vertical flex column, gap `8px`.
- Default item height without hint: `40px`.
- Hint item height: `61px`.
- Input row: horizontal flex row, align start, gap `16px`.
- Radio input: `40px` by `40px`.
- Default border: `2px solid #1F1F1F`.
- Focus border: `4px solid #1F1F1F`.
- Focus ring: `0 0 0 3px #FFDD00`.
- Border radius: `1000px`.
- Selected dot: `20px` by `20px`, centred, `#1F1F1F`.
- Content column: flex column, justify centre, padding `4px 0`, gap `5px`.
- Content column width: `456px` when the input row is `512px` wide.
- Content column width: `584px` when the input row stretches to `640px` wide.

## Typography

- Label: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Hint: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Component labels and hints should not be bold.

## Error State

- Group error state keeps width `640px`.
- Add `24px` left padding.
- Add a `4px` red left bar using `#D43F46`.
- Error text: Gotham Rounded Bold, `16px`, `24px` line height, `#D43F46`.
- Error text row has `0 0 5px` bottom padding.
- In error state, the radio buttons list width becomes `616px`.

## Small Variant

- Group width remains `640px`.
- Radio item height: `32px`.
- Input row height: `32px`.
- Radio input: `32px` by `32px`.
- Small label: Gotham Rounded Book, `14px`, `24px` line height, `#333333`.
- Content column width: `592px`.
- Selected dot remains visually centred.

## Reveal Variant

- Reveal item height: `156px`.
- Radio row remains `640px` by `40px`.
- Reveal panel: `640px` wide, `108px` high, padding `0 0 0 18px`, gap `36px`.
- Reveal left border: `4px` wide, `#B1B4B6`.
- Nested text input area: `582px` wide, `108px` high, gap `8px`.
- Nested text input: `582px` wide, `48px` high, padding `12px 16px`, `2px solid #1F1F1F`.

## Prototype Notes

- Use `.nrw-radio-group`, `.nrw-radio-group__label`, `.nrw-radio-group__hint`, `.nrw-radio-group__error`, `.nrw-radios`, `.nrw-radio-option`, `.nrw-radio-item`, `.nrw-radio-control`, `.nrw-radio-content`, `.nrw-radio-label`, `.nrw-radio-hint`, and `.nrw-radio-reveal` from `styles/nrw.css`.
- Add `.nrw-radio-group--error` to the group when showing validation errors.
- Add `.nrw-radio-group--small` to the group for the small radio variant.
- Keep the native radio input in the markup for accessibility, then visually style the adjacent `.nrw-radio-control`.
- Use `fieldset` and `legend` around the radio group.
- Conditional reveal content should be associated with the relevant option and only shown when selected.
