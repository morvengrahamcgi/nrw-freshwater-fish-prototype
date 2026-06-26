# Page Heading

## Source

- Figma export: `Desktop / Headings`

## Purpose

Use the page heading band immediately below the top nav to identify the current service section or page group.

## Desktop Layout

- Outer component width: full page width, exported at `1440px`.
- Height: `123px`.
- Background: `#007485`.
- Layout: vertical flex column, centred, padding `32px 0`, gap `16px`.
- Decorative white pattern appears on the right using `assets/page-heading-pattern.svg`.
- Pattern asset size: `685px` wide by `123px` high.
- The SVG paths carry `5%` opacity, matching the Figma export, and are clipped inside the heading band.
- Elements group: `1020px` wide, `59px` high, padding `0 16px`, gap `8px`.
- Heading row: `988px` wide, `59px` high, horizontal flex row, align centre, gap `16px`.
- Page title: `770px` wide, `59px` high in the desktop export.
- Inline content row is hidden in the default variant.
- Dropdown icon is hidden in the default variant.
- Button is hidden in the default variant.

## Long Title Variant

Use this variant when the H1 wraps to two lines, as shown in the `Template` Figma export for Freshwater Fish Flows.

- Outer component width: full page width, exported at `1440px`.
- Height: `182px`.
- Background: `#007485`.
- Layout: vertical flex column, centred, padding `32px 0`, gap `16px`.
- Elements group: `1020px` wide, `118px` high, padding `0 16px`, gap `8px`.
- Heading row: `988px` wide, `118px` high.
- Page title: `770px` wide, `118px` high.
- H1 stays Gotham Rounded Bold, `48px`, `59px` line height, `#FFFFFF`.
- Use `.nrw-page-heading--long` with the standard page heading classes.

## Typography

- Figma export labels this as Montserrat, but NRW prototype rules override this to Gotham Rounded.
- Use H1: Gotham Rounded Bold, `48px`, `59px` line height.
- Colour: `#FFFFFF`.

## Prototype Notes

- Use `templates/includes/page-heading.html` for the default implementation.
- Use `.nrw-page-heading`, `.nrw-page-heading__inner`, `.nrw-page-heading__content`, and `.nrw-page-heading__title` from `styles/nrw.css`.
- Use `.nrw-page-heading--long` when the approved Figma frame shows a two-line H1 and `182px` heading band.
- The pattern is applied in CSS using `.nrw-page-heading::before` and `assets/page-heading-pattern.svg`.
- If a future Figma screen shows inline content, dropdown, or a button visible inside the band, document that as a separate page-heading variant before using it.
