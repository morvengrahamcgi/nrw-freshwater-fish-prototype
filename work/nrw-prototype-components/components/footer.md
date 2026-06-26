# Footer

## Source

- Figma export: `Desktop / Footer`

## Purpose

Use the footer at the bottom of NRW prototype pages for service links, NRW identity, and copyright.

## Desktop Layout

- Outer component width: full page width, exported at `1600px`.
- Height: `233px`.
- Background: `#58595B`.
- Layout: vertical flex column, align centre, padding `0 0 40px`, gap `40px`.
- Top rule: full width, `4px` high, `#358728`.
- Container: `1020px` wide, `149px` high.
- Content: `1020px` wide, `149px` high, padding `0 16px`, gap `32px`.
- Links row: `752px` wide, `40px` high, horizontal flex row, align centre, gap `24px`.
- Link dividers: `1px` wide, `40px` high, `#E3E3E3`.
- Horizontal divider: `988px` wide, `1px` high, `#A1A1A1`.
- Logo and rights row: `988px` wide, `44px` high, `justify-content: space-between`.
- Footer NRW logo: `257.12px` wide, `44px` high.
- Copyright text: `260px` wide, `24px` high, right aligned.

## Typography

- Footer links: Gotham Rounded Bold, `16px`, `24px` line height, `#FFFFFF`.
- Figma export labels footer links as Montserrat, but NRW prototype rules override this to Gotham Rounded.
- Copyright: Gotham Rounded Book, `14px`, `24px` line height, `#FFFFFF`.

## Prototype Notes

- Use `templates/includes/footer.html` for the default implementation.
- Use `.nrw-footer`, `.nrw-footer__rule`, `.nrw-footer__inner`, `.nrw-footer__links`, `.nrw-footer__divider`, `.nrw-footer__brand-row`, `.nrw-footer__logo`, and `.nrw-footer__copyright` from `styles/nrw.css`.
- The feedback strip is not part of this footer export. Keep it as a separate component/pattern when needed.
- Replace the temporary text logo with the official footer logo asset when available.
