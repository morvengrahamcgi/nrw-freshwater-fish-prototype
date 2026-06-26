# Buttons

## Source

- Figma export supplied by NRW design system.
- GOV.UK baseline: use GOV.UK button semantics and behaviour, with NRW visual styling.

## Purpose

Use buttons to help users carry out an action.

## Typography

- Buttons are a documented exception to the general component text rule.
- Use Gotham Rounded Bold.
- Large button text: `18px`, `24px` line height.
- Medium button text: `16px`, `24px` line height.
- Small button text: `14px`, `24px` line height.
- Text and icon align to the `24px` text line.

## Sizes

| Size | Height | Padding | Gap | Icon |
| --- | --- | --- | --- | --- |
| Large | `48px` | `12px 16px` | `12px` | `24px` |
| Medium | `40px` | `8px 12px` | `12px` | `24px` |
| Small | `36px` | `6px 12px` | `8px` | `16px` |

## Types

| Type | Default background | Border | Text and icon |
| --- | --- | --- | --- |
| Primary | `#358728` | none | `#FFFFFF` |
| Secondary | `#FFFFFF` | `2px solid #358728` | `#358728` |
| Tertiary | `#FFFFFF` | `2px solid #58595B` plus inset shadow `0 -2px 0 #929191` | `#58595B` |
| Danger | `#D43F46` | none | `#FFFFFF` |

## States

- Primary hover: background `#26601C`, text and icon `#FFFFFF`.
- Secondary hover: background `#26601C`, border `#26601C`, text and icon `#FFFFFF`.
- Tertiary hover: background `#58595B`, text and icon `#FFFFFF`.
- Danger hover: background `#942C31` for large and `#55191C` for medium.
- Focus and pressed: background `#FFDD00`, text and icon `#0B0C0C`, shadow `0 5px 0 #0B0C0C`.
- Loading: keep the default button background and overlay with `rgba(11, 27, 8, 0.9)` plus a `24px` loader.
- Border radius: `4px`.

## Icons

- Use the chevron-right icon when the approved Figma button variant includes it.
- Large and medium icon size: `24px`.
- Small icon size: `16px`.
- Icons use the same colour as the button text.

## Prototype Notes

- Use `.nrw-button` as the base class.
- Add one type class: `.nrw-button--primary`, `.nrw-button--secondary`, `.nrw-button--tertiary`, or `.nrw-button--danger`.
- Add one size class only when not using the large default: `.nrw-button--medium` or `.nrw-button--small`.
- Use `.nrw-button-row` for Back and Continue button groups.
- Use the outlined secondary button for Back and the primary green button for Continue.
