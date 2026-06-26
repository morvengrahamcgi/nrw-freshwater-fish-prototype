# Text Input

## Source

- Figma export: `Building blocks/Text`
- GOV.UK baseline: use GOV.UK text input semantics, labels, hints, validation, and error messages.

## Purpose

Use text inputs when users need to enter a short piece of information, such as a name, reference, email address, or short label.

## Layout

- Input width: `640px`.
- Input height: `38px`.
- Padding: `8px 16px 8px 12px`.
- Background: `#FFFFFF`.
- Border: `2px solid #1F1F1F`.
- Input text uses Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Hint text width: `640px`.
- Hint text uses Gotham Rounded Book, `16px`, `24px` line height, `#333333`.

## Prototype Notes

- Use `.nrw-text-input` from `styles/nrw.css`.
- Keep visible labels outside the input using standard GOV.UK form structure.
- Put whole-question information under the question heading as `.nrw-application-question__body`, not as field-level hint text.
- Use field hint text only when the help belongs specifically to the input control.
- Use `autocomplete`, `inputmode`, and type attributes where they improve the experience.
- For longer responses, use `.nrw-textarea` instead.
- For numeric values with a default unit and a link-style unit switch, use `components/unit-switch-input.md` instead of radio buttons.
