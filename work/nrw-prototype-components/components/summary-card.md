# Summary Card

## Source

- Figma export: `Summary list or card`
- GOV.UK baseline: use GOV.UK summary list and summary card guidance.

## Purpose

Use a summary list to summarise information, such as a user's responses at the end of a form.

Use summary cards to show multiple summary lists that describe the same type of thing, such as people, locations, activities, documents, or application parts. Card actions apply to the whole summary list.

## Card Layout

- Card width: `640px`.
- Card border: `1px solid #A1A1A1`.
- Header row height: `56px`.
- Header background: `#F4F4F4`.
- Header padding: `0 24px`.
- Header inner row: `592px` wide, `56px` high, `16px 0` padding, `10px` gap.
- Title area: full available width, `0 8px` padding, when there is no card action.
- When a card action is present, keep the title and action in the same 592px header row, with the action right aligned.
- Card title: Gotham Rounded Bold, `18px`, `24px` line height, `#333333`.
- Card action link: Gotham Rounded Bold, `16px`, `24px` line height, `#007485`, right aligned.

## Content Layout

- Content area width: `640px`.
- Content background: `#FFFFFF`.
- Two content columns: `320px` each.
- Row height: `56px` to `57px`.
- Left/key cells: `24px` outer left padding plus `16px 8px` inner cell padding.
- Right/value cells: `24px` outer right padding plus `16px 8px` inner cell padding.
- Inner cell padding: `16px 8px`.
- Key text: Gotham Rounded Bold, `16px`, `24px` line height, `#333333`.
- Value text: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Row dividers: `2px solid #A1A1A1` between rows.

## Prototype Notes

- Use `.nrw-summary-card`, `.nrw-summary-card__header`, `.nrw-summary-card__title`, `.nrw-summary-card__actions`, `.nrw-summary-list`, `.nrw-summary-list__row`, `.nrw-summary-list__key`, and `.nrw-summary-list__value` from `styles/nrw.css`.
- Use semantic `dl`, `dt`, and `dd` markup for the summary list.
- Use card-level actions only for actions that affect the whole card.
- Use row-level change links only when the action applies to a single answer.
- Keep summary values short enough to scan; wrap long text naturally rather than shrinking type.

## Three-Column Row Action Variant

- Use `.nrw-summary-list--with-actions` when each row needs a key, value, and action link.
- Width: `770px`.
- Columns: three equal columns of `256.67px`.
- Row height: `57px`.
- Action link text: Gotham Rounded Bold, `16px`, `24px` line height, `#007485`, right aligned.
- Row dividers: `2px solid #A1A1A1`.
