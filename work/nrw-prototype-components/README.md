# NRW Prototype Components

Reusable starter components and page templates for Codex-built NRW prototypes.

Use this folder as the practical source of truth alongside `outputs/codex-prototype-design-system.md`.

## How To Use

When asking Codex to build a prototype, say:

```text
Use work/nrw-prototype-components as the source of truth for layout, header, footer, page heading, components, and page templates.
Use outputs/codex-prototype-design-system.md for the design rules.
```

## Structure

- `styles/nrw.css`: shared NRW prototype styling.
- `assets/nrw-logo.svg`: official NRW header logo asset.
- `assets/page-heading-pattern.svg`: decorative page-heading pattern asset.
- `components/top-nav.md`: documented top-nav component source notes.
- `components/page-heading.md`: documented page-heading/header band source notes.
- `components/footer.md`: documented footer component source notes.
- `components/radios.md`: documented radio item, hint, focus, selected, and reveal variants.
- `components/checkboxes.md`: documented checkbox input, item, focus, disabled, small, and reveal variants.
- `components/file-upload.md`: documented file upload drop zone, browse button, drag, focus, and selected-file table variants.
- `components/text-input.md`: documented compact text input field and hint rules.
- `components/unit-switch-input.md`: documented unit switch text input for numeric values with a default unit and link-style unit switch.
- `components/summary-card.md`: documented summary list and summary card variant for review pages.
- `components/buttons.md`: documented button sizes, types, states, icons, and typography.
- `templates/includes/header.html`: approved top navigation starter.
- `templates/includes/page-heading.html`: aqua page heading band.
- `templates/includes/footer.html`: feedback row and footer.
- `templates/layouts/main.html`: full page shell.
- `templates/pages/question-page.html`: single question pattern.
- `templates/pages/multiple-questions.html`: dependent follow-up question pattern.
- `templates/pages/checkbox-confirmation.html`: data/privacy checkbox pattern.
- `templates/pages/file-upload.html`: file upload question pattern.
- `templates/pages/screening-checkbox-question.html`: screening question with checkbox options and a none-of-the-above separator.
- `templates/pages/summary-card.html`: summary card pattern for grouped review information.
- `templates/pages/long-form-multiple-questions.html`: wider multi-question pattern with radio options, text input, and row-level summary actions.
- `examples/confidentiality-flow.html`: example assembled flow.
- `examples/buttons.html`: visual example page for button variants.

## Current Defaults

- Use GOV.UK component semantics and behaviour.
- Apply NRW typography, colour, header, footer, and page shell treatment.
- Use Gotham Rounded Book for component text unless a component exception says otherwise.
- Buttons are an exception: use Gotham Rounded Bold.
- Top nav uses the documented desktop Figma export: 72px high, #F4F4F4 background, 1020px centred inner group, 297.41px logo block, 112px language block, and 94px sign-in block.
- Page heading uses the documented desktop Figma export: 123px high, #007485 background, 1020px centred elements group, 988px heading row, and 48px white H1 text.
- Long page headings use the documented template variant: 182px high, 1020px centred elements group, 988px heading row, and 770px by 118px two-line H1 area.
- Footer uses the documented desktop Figma export: 233px high, #58595B background, 4px green top rule, 1020px centred content, 988px divider, and 257.12px footer logo.
- Radios use the documented Figma exports: 640px group, 40px medium control, 32px small control, 16px input-to-label gap, 20px selected dot, 3px yellow focus ring, group error state, and body-weight option labels.
- Checkboxes use the documented Figma exports: 40px medium control, 32px small control, 16px input-to-label gap, 25px by 20px medium selected icon, and body-weight labels.
- File upload uses the documented Figma export: 640px drop zone, 172px minimum height, 24px padding, black dashed border, grey hover/focus background, medium green browse button, and selected-file table.
- Screening checkbox pages use a 1020px content wrapper with 48px vertical padding, a 640px question block, 24px spacing between intro text and controls, and a separate `or` divider before `None of the above`.
- Long-form multiple-question pages can use 770px question blocks with 24px gaps, 640px nested text fields, and 770px radio groups where the visible option content is 512px wide.
- Application question templates use the supplied Template layout: a 1020px content wrapper with `48px 16px` padding and `32px` gap, a 988px column row, a left-justified 640px content column, H2 at 30px/37px, visible body copy at 16px/24px when supporting text is present, a 640px radio group, and a 303px button group below the column container. Use 16px between question heading and supporting copy, 24px between question text and form control, 24px between radio options, and 24px from action row to body link. Section headings are only needed where multiple questions appear on a page.
- Whole-question information must sit directly under the question heading as supporting body copy, using `.nrw-application-question__body`. Do not use field-level hint text for information that explains the whole question.
- Progressive same-screen follow-up questions must use separate full question blocks in the same left-justified 640px column. Use `.nrw-question-stack` for the 56px gap between question blocks and `.nrw-question-block--progressive` for the 24px gap between the question text group and control. When a question has supporting body copy, group the heading and body copy in `.nrw-question-block__text`. Do not place substantial follow-up questions inside an indented radio reveal.
- Multi-section prototypes should open on a task list page. Use the `Summary=Card, Width=Default` component for each grouped section: 640px summary cards, grey 56px header row, semantic summary-list rows, row links into the journey, and status text. Every journey page should include a `Go back to task list` link.
- Add-to-a-list pages should ask for one item at a time, then use a progressive added-items state with a compact summary list and a Yes/No question asking whether the user needs to add another item.
- The fish add-to-a-list variant uses 56px between the main heading section and the fish questions, 56px between fish question blocks, 24px between each question text group and its control, full-width 640px by 48px inputs/selects, and a link-style length/weight switch. The first state uses the standard primary `Save and continue` button, not a separate add button. The added-fish state uses `You have added X type(s) of fish`, Change and Remove actions, and `Do you need to add another type of fish?`.
- Checkbox confirmation pages use a single H2, body copy, one required NRW checkbox, and standard Back/Save controls. Use this for privacy acknowledgements and declarations.
- Text inputs use the documented Figma export: 640px width, 38px height, 2px dark border, and `8px 16px 8px 12px` padding.
- Unit switch inputs use the documented Figma export: 640px component, 24px gap, visible 16px bold unit label, 640px by 48px text input with `12px 16px` padding, and a 16px bold link-style switch action underneath.
- Summary cards use the documented Figma export: 640px card, 1px grey border, 56px grey header, 24px side padding, full-width 18px bold title when there is no card action, 16px bold card action when present, and two-column summary rows.
- Buttons use the documented NRW exception: Gotham Rounded Bold, 4px radius, green primary, outlined secondary, grey tertiary, red danger, and yellow focus/pressed state.
- Use `assets/nrw-logo.svg` for the header logo.

## Useful Next Additions

- Add GOV.UK Prototype Kit Nunjucks versions of these templates.
- Add approved header/footer screenshots or Figma frame links.
- Add page templates for check answers, confirmation, task list, tables, modals, toasts, and badges.
