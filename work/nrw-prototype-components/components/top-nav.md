# Top Nav

## Source

- Figma export: `Desktop / Top Nav`
- GOV.UK baseline: use GOV.UK header and service navigation principles for semantics and accessibility, but apply the NRW visual treatment.

## Purpose

Use the top nav at the top of NRW prototype pages to provide the NRW logo, language switch, and sign-in entry point.

## Desktop Layout

- Outer component width: full page width, exported at `1440px`.
- Height: `72px`.
- Background: `#F4F4F4`.
- Inner top-nav group: `1020px` wide, centred with `margin: 0 auto`.
- Inner group layout: horizontal flex row, `justify-content: space-between`, `align-items: center`.
- Logo block: `297.41px` wide, `72px` high, background `#F4F4F4`.
- Logo frame: `297.41px` wide, `57px` high, padding `6px 16px`.
- Logo asset: `assets/nrw-logo.svg`, `265.41px` wide, `45px` high.
- Selections group: `206px` wide, `72px` high.
- Language block: `112px` wide, `72px` high, padding `0 20px`.
- Language link frame: `72px` wide, `36px` high, padding `6px 0`.
- Sign-in block: `94px` wide, `72px` high, padding `0 20px`.
- Sign-in text frame: `54px` wide, `36px` high, padding `6px 0`.
- Sign-in link: `54px` wide, `24px` high.
- Login icon is hidden in this desktop variant.
- Account name, logout, and menu rows are hidden in this desktop variant.

## Typography

- Language toggle: Gotham Rounded Book, `16px`, `24px` line height, `#007485`.
- Sign-in text: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Hidden account name text uses `#58595B`.

## Prototype Notes

- Use `templates/includes/header.html` for the default implementation.
- Use `.nrw-top-nav`, `.nrw-top-nav__inner`, `.nrw-logo-block`, `.nrw-nav-actions`, `.nrw-language-block`, and `.nrw-sign-in-block` from `styles/nrw.css`.
- Use `assets/nrw-logo.svg` for the header logo.
