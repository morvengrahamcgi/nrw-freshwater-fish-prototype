# File Upload

## Source

- Figma export: `Building block components / File upload area`
- GOV.UK baseline: use GOV.UK file upload semantics and behaviour.

## Purpose

Use file upload when users need to attach a document, image, or supporting evidence to a service.

## Drop Zone Layout

- Drop zone width: `640px`.
- Minimum height: `172px`.
- Padding: `24px`.
- Gap between instruction text and browse button: `16px`.
- Background: `#FFFFFF`.
- Default border: `2px dashed #1F1F1F`.
- Instruction text: Gotham Rounded Book, `20px`, `24px` line height, `#333333`.
- Instruction text says `Drag and drop or`.
- Browse button uses the NRW medium primary button:
  - Height: `40px`.
  - Padding: `8px 12px`.
  - Background: `#358728`.
  - Hover background: `#26601C`.
  - Text: Gotham Rounded Bold, `16px`, `24px` line height, `#FFFFFF`.
  - Border radius: `4px`.

## States

- Hover: background `#F4F4F4`, border `3px dashed #1F1F1F`.
- File drop or drag-over: background `#F4F4F4`, border `3px solid #1F1F1F`.
- Focus: background `#F4F4F4`, border `3px solid #1F1F1F`, shadow `0 0 0 3px #FFDD00`.
- Focus or pressed browse button: background `#FFDD00`, text `#0B0C0C`, shadow `0 5px 0 #0B0C0C`.

## Selected File Table

- Table width: `672px` in the Figma component set; use `min(672px, 100%)` in prototypes.
- Header row top padding: `24px`.
- Header text: H4 styling, Gotham Rounded Bold, `16px`, `20px` line height, `#58595B`.
- Row top padding: `12px`.
- Row text: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Column headings: `Filename`, `Size`, `Status`.
- Dividers: `1px solid #E3E3E3`.
- File status badges can use the NRW badge styles when a status needs to be shown.

## Prototype Notes

- Use `.nrw-file-upload`, `.nrw-file-upload__dropzone`, `.nrw-file-upload__input`, `.nrw-file-upload__button`, and `.nrw-file-upload__files` from `styles/nrw.css`.
- Keep the native file input in the markup for accessibility.
- Label the native file input with the visible browse button.
- Use the GOV.UK file upload validation pattern for missing files, wrong file types, files that are too large, or upload failures.
- Do not use the purple dashed Figma wrapper in prototypes; it is only the design-system component frame.
