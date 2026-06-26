# NRW Design System

Use this file as the design contract for Codex-built prototypes across NRW projects. It translates the existing Figma design system and NRW defined guidelines into practical rules, patterns, accessibility expectations, and prototype build instructions.

This system closely follows the GOV.UK Design System. Prefer GOV.UK styles, components, and patterns unless there is a documented NRW variation.

## 1. Project Setup

### Source Of Truth

Add the durable references Codex should use before building prototypes.

- Canonical Figma design system: `https://www.figma.com/design/NuGro5Sz8e8bDB4OkJfb2a/Natural-Resource-Wales---Design-System?node-id=175-15714&p=f&t=rfGixuIDpg7SJmOz-0`
- Figma prototype or screen examples: `https://www.figma.com/design/oFYy4KSeEeCvdJrmD7bilj/Marine---Design-system?node-id=515-20049&t=t08jsgavopmIqdQU-4`
- Reusable Codex component and template folder: `work/nrw-prototype-components/`
- Component documentation: `https://design-system.service.gov.uk/components/`
- Existing service examples: `https://home.naturalresources.wales/en/applications/marine-band-1/2b25bbb7-6551-4b8e-92c2-ec7225578d0e/summary`
- Accessibility guidance: `https://design-system.service.gov.uk/accessibility/`
- Digital Service Standard for Wales: `https://digitalpublicservices.gov.wales/guidance-and-standards/digital-service-standard-wales`

### Project Scope

This file is transferable between NRW projects. Treat it as the shared NRW prototype design-system guide rather than a guide for one named service.

When building a specific service prototype, add the service name, user journey, and any service-specific Figma examples in the prototype brief, not in this shared file.

### Prototype Stack

Use the GOV.UK Prototype Kit by default for NRW prototypes.

Before creating new pages, copy from or adapt the reusable files in `work/nrw-prototype-components/`. Treat that folder as the local practical starter kit for approved header, footer, page heading, form controls, button styling, and page templates.

Only use another stack when the user explicitly asks for it or when the prototype requires behaviour that the GOV.UK Prototype Kit cannot reasonably support.

### Relationship To GOV.UK

Use GOV.UK as the baseline for:

- layout, spacing, focus states, and form behaviour
- reusable components such as buttons, text inputs, radios, checkboxes, tables, tags, panels, summary lists, task lists, headers, footers, breadcrumbs, back links, and error summaries
- service patterns such as question pages, check answers, confirmation pages, start pages, validation errors, and multi-step task flows

Only diverge from GOV.UK when the Figma design system explicitly documents a project-specific pattern.

### Relationship To The Digital Service Standard For Wales

Use the Digital Service Standard for Wales as the service-quality baseline for NRW prototypes. The standard defines what good public services look like in Wales and groups 12 points across 3 categories: meet user needs, create digital teams, and use the right technology.

Codex prototypes should support the standard by making design choices that are:

- user-centred and based on real needs
- bilingual by default, considering Welsh and English from the start
- inclusive, accessible, and usable by people with different digital skills, access needs, and circumstances
- joined up across digital, phone, in-person, and offline service channels where the wider journey requires it
- easy to test, learn from, and iterate
- safe with personal data, privacy, security, and ethical risks
- measurable, so teams can use evidence and data to make decisions

## 2. Welsh Digital Service Standard Checks

Use these checks before, during, and after prototype work.

### Meet User Needs

- Focus on outcomes that benefit people in Wales, not only business or technical requirements.
- Consider the current and future wellbeing of people in Wales, including social, economic, environmental, and cultural wellbeing.
- Design Welsh and English language journeys from the start. Do not add Welsh language considerations after the design has already been decided.
- Test Welsh language content and bilingual service switching with users as early as possible.
- Base prototype flows on user needs, not internal structures, existing systems, or organisational boundaries.
- Look at the whole journey from start to finish, including online, phone, in-person, assisted digital, and offline channels.
- Include accessibility and digital inclusion needs in the prototype scope.
- Provide non-digital or assisted routes where users may have low digital skills, limited access, or other barriers.

### Create Digital Teams

- Make the service owner, decision-maker, or product owner clear when documenting prototype assumptions.
- Capture which disciplines should review the prototype: user research, service design, content design, product, accessibility, policy, operations, legal, technical, and subject matter experts as needed.
- Use prototypes to test ideas early and cheaply with users.
- Build the smallest realistic version of the journey that can answer the research or design question.
- Iterate after usability testing, accessibility review, analytics, operational feedback, and stakeholder review.
- Work in the open where safe: document assumptions, design decisions, reusable patterns, and learning from each round.

### Use The Right Technology

- Use scalable technology choices for prototypes when the prototype may become a reference for production delivery.
- Consider ethics, privacy, and security throughout, especially when journeys involve personal data, case data, identity, payments, permits, enforcement, or vulnerable users.
- Use data to make design decisions, including research findings, analytics, service data, call-centre evidence, operational insight, and accessibility findings.
- Do not use real personal data in prototypes.
- Make clear which parts of the prototype are realistic service behaviour and which parts are mocked.

## 3. How To Use This File With Codex

When asking Codex to make a prototype, provide:

1. The user goal or task.
2. The screen or flow to create.
3. The relevant Figma frame, component, or screenshot.
4. The expected interactivity level.
5. Any data, content, or edge cases the prototype should include.

Example prompt:

```text
Build an interactive prototype for the eligibility question flow.
Use the design rules in outputs/codex-prototype-design-system.md.
Match the Figma design system and GOV.UK patterns.
Include validation errors, back links, a check answers page, and a confirmation page.
Use realistic sample content but no real user data.
```

## 4. Prototype Principles

### Make It Service-Like

- Build the actual task flow, not a landing page.
- Start with the first meaningful user action.
- Use realistic service content and data.
- Include common states: default, hover, focus, error, empty, loading, success, and unavailable where relevant.
- Prefer plain, direct content over marketing or decorative language.

### Keep GOV.UK Behaviour

- Use one thing per page for important questions.
- Use clear page headings that match the task.
- Use back links for linear journeys.
- Use breadcrumbs only where the information architecture needs them.
- Use summary lists for review pages.
- Use panels for confirmation moments.
- Use error summaries and inline error messages together.

### Design For Research

- Make the path realistic enough that participants can suspend disbelief.
- Avoid dead ends unless the test requires them.
- Include enough branching to test the decision or behaviour being studied.
- Mark assumptions in comments or notes, not in visible UI.

## 5. Visual Foundations

### Typography

- Use Gotham Rounded for prototype typography.
- Use the project type scale from Figma where it adds more detail than the rules below.
- Do not fall back to GOV.UK typography unless Gotham Rounded is unavailable in the prototype environment.
- Use sentence case for headings and labels.
- Avoid decorative type treatments.
- Keep body copy concise and scannable.

#### Headings

- Font family: Gotham Rounded.
- Font weight: Bold.
- Colour: `#58595B`.
- H1: `48px` on screens wider than `768px`; usually used in the page header.
- H2: `30px`.
- H3: `24px`.
- H4: `16px`.

#### Body Text

- Font family: Gotham Rounded.
- Font weight: Book.
- Colour: `#333333`.
- Default size: `16px` medium.
- Line height: `24px`.
- Paragraph spacing: `16px`.
- Small body text: `14px` with `24px` line height.
- Component text, including labels, links, checkbox labels, radio labels, and validation text, should use Gotham Rounded Book/body weight unless a supplied Figma component explicitly documents a bold exception.
- Button text is a documented exception: use Gotham Rounded Bold for NRW buttons.
- If pasted Figma CSS shows Montserrat for headings or links, use Gotham Rounded unless the design system is later updated to document Montserrat as an exception.

### Colour

- Use the Figma colour tokens as the source of truth.
- If no project override exists, follow GOV.UK colour usage.
- Do not introduce new colours for prototype convenience.
- Never rely on colour alone to communicate meaning.

#### Current Colour Tokens From Layout Source

- Page background: `#FFFFFF`.
- Header background: `#F4F4F4`.
- Heading text: `#58595B`.
- Body text: `#333333`.
- Link default: `#007485`.
- Heading band background: `#007485`.
- Primary action and footer accent: `#358728`.
- Footer background: `#58595B`.
- Footer divider: `#A1A1A1`.
- Pale divider: `#E3E3E3`.
- Confirmation dark: `#128300`.
- Confirmation light: `#F0F5F4`.
- Error dark: `#D43F46`.
- Error light: `#FBECED`.
- Warning dark: `#FF9447`.
- Warning darker: `#D04716`.
- Warning light: `#FFF4ED`.
- Focus yellow: `#FFDD00`.
- Disabled badge grey: `#E9E9EA`.

### Spacing And Layout

- Use the Figma spacing scale.
- If no project override exists, follow GOV.UK spacing and grid conventions.
- Keep forms narrow enough to read comfortably.
- Keep task pages calm and uncluttered.
- Avoid nested cards and decorative containers.

#### Desktop Shell Layout

- Desktop design width may be `1280px` or `1440px` depending on the approved Figma template.
- Do not stretch the core content to match the full desktop frame width.
- Main content container: `1020px` wide, centred.
- Inner content width inside the container: `988px` after `16px` horizontal padding.
- Top navigation height: `72px`.
- Top navigation background: `#F4F4F4`.
- Top navigation content group: `1020px` wide, centred, `72px` high, with logo block on the left and selections on the right.
- Header logo area: `297.41px` wide by `72px` high.
- Header logo frame: `297.41px` wide by `57px` high with `6px 16px` padding.
- Header logo asset: `work/nrw-prototype-components/assets/nrw-logo.svg`, approximately `265.41px` wide by `45px` high.
- Always use the NRW logo asset in the logo area. Do not substitute plain text for the logo in prototypes.
- Header controls use `20px` horizontal padding and `24px` icon/text height.
- Header selections group: `206px` wide by `72px` high.
- Language toggle width: `72px`.
- Language block: `112px` wide by `72px` high with `0px 20px` padding.
- Sign-in block: `94px` wide by `72px` high with `0px 20px` padding.
- Sign-in text group: `54px` wide by `24px` high.
- Hide the login icon in the default desktop top-nav variant.
- Account name, logout, and menu rows are hidden in the default desktop top-nav variant unless the Figma template shows them active.
- Primary page heading band height: `123px` on desktop.
- Heading band padding: `32px 0`.
- Heading band background: `#007485`.
- Heading band content uses the `1020px` centred elements group with `16px` horizontal padding.
- Heading band heading row is `988px` wide by `59px` high.
- Heading band page title is `770px` wide by `59px` high in the desktop export.
- Heading band title uses H1: Gotham Rounded Bold, `48px`, `59px` line height, `#FFFFFF`.
- Heading band includes `work/nrw-prototype-components/assets/page-heading-pattern.svg` on the right, clipped inside the band and positioned behind the title content. The SVG paths use `5%` opacity.
- Inline content, dropdown icon, and button variants are hidden in the default page-heading variant unless the Figma template shows them active.
- Long page heading variant height: `182px` on desktop.
- Long page heading variant uses `32px 0` padding, `#007485` background, and the decorative page-heading pattern.
- Long page heading elements group: `1020px` wide, `118px` high, with `0 16px` padding and `8px` gap.
- Long page heading row: `988px` wide by `118px` high.
- Long page heading title area: `770px` wide by `118px` high.
- Long page heading title uses H1: Gotham Rounded Bold, `48px`, `59px` line height, `#FFFFFF`.
- Footer height: `233px` on desktop.
- Footer background: `#58595B`.
- Footer top rule: `4px` high, `#358728`.
- Footer content uses the `1020px` centred container with `16px` horizontal padding.
- Footer links row is `752px` wide by `40px` high, with `24px` gaps and `1px` by `40px` dividers in `#E3E3E3`.
- Footer divider is `988px` wide by `1px` high in `#A1A1A1`.
- Footer logo and rights row is `988px` wide by `44px` high.
- Footer logo is `257.12px` wide by `44px` high.
- Footer link text uses Gotham Rounded Bold, `16px`, `24px` line height, `#FFFFFF`.
- Footer copyright uses Gotham Rounded Book, `14px`, `24px` line height, `#FFFFFF`, right aligned.
- Main content area starts with `48px` top padding.
- Main content column width: `640px`.
- Related links column width: `316px`.
- Main two-column gap: `40px`.
- Template content wrapper: `1020px` wide with `48px 16px` padding and `32px` gap between the column container and button group.
- Template column row: `988px` wide, horizontal layout, `40px` gap.
- Template content column: `640px` wide, left-justified inside the `988px` column row with `margin: 0`.
- Template content column uses `40px` gap only between major content sections.
- Template application question frame: `640px` wide.
- Template application question H2: Gotham Rounded Bold, `30px`, `37px` line height, `#58595B`.
- Template question heading to supporting body-copy gap: `16px`.
- Template body copy: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Template question text area to form component gap: `24px`.
- Template radio group: `640px` wide, `24px` gap between options.
- Template button group is a sibling below the column container, not inside the 640px text frame. The parent wrapper gives `32px` between the column container and button group.
- Template action row: `303px` wide, `48px` high, `16px` gap, with `80px` Back button and `207px` Save and continue button.
- Template action row to body link gap: `24px`.
- If the Figma template hides the Save and continue chevron/icon, use text only in the button.
- Task-list links may sit inside the button group below the action row when shown by the approved template. Do not replace this with the wider standalone feedback strip.
- Standard vertical content gap in the page body: `40px`.
- Text-frame gap between heading and body copy: `16px`.
- Section headings are only used when there are multiple questions on a page. For a single-question page, use the question heading only; do not add a separate visible section heading.
- Multiple-question content wrapper: `1020px` wide with `48px 16px` padding.
- Multiple-question content column: `640px` wide.
- Multiple-question stack gap: `56px` between question blocks.
- Multiple-question block gap: `24px` between the heading/body copy group and the form control.
- Multiple-question heading/body copy group gap: `16px`.
- Screening checkbox page wrapper: `1020px` wide with `48px 16px` padding.
- Screening checkbox question block: `640px` wide, `24px` gap between the intro text block and checkbox group.
- Screening checkbox intro text block: `640px` wide, `16px` gap between the H2 question and body copy.
- Screening checkbox group: `640px` wide, `16px` gap between the group label and checkbox list.
- Screening checkbox group label: `582px` wide, Gotham Rounded Bold, `16px`, `24px` line height, `#333333`.
- Screening checkbox list: `640px` wide, `24px` gap between options.
- Screening checkbox none-of-the-above separator: plain body text `or`, `40px` wide by `20px` high with `0 10px` horizontal padding.
- Screening checkbox action row: Back button `80px` wide and Continue button `119px` wide, both `48px` high, with `16px` gap.
- Multiple-question text area: `640px` wide, `180px` high, `12px 16px` padding, `2px solid #1F1F1F`.
- Multiple-question text area hint or helper row: `640px` wide, `24px` high.
- Long form content wrapper: `1200px` wide with `48px 16px` padding.
- Long form question block width: `770px`.
- Long form question block gap: `24px`.
- Long form question heading uses H2 styling: `30px` bold, `37px` line height.
- Long form question intro block can be `770px` wide with a `16px` gap between heading and body copy.
- Long form radio group can be `770px` wide with `24px` gaps between options.
- Long form radio visible input row can be `512px` wide, with a `40px` radio input, `16px` gap, and `456px` label content.
- Long form text input question can use a `770px` question block with a nested `640px` title/input group.
- Short text input width: `640px`.
- Short text input height: `38px`.
- Short text input padding: `8px 16px 8px 12px`.
- Short text input border: `2px solid #1F1F1F`.
- Short text input background: `#FFFFFF`.
- Short text input should use Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Text input hint text: `640px` wide, Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Unit switch text input component: `640px` wide with `24px` gap between the input group and switch link.
- Unit switch label: Gotham Rounded Bold, `16px`, `24px` line height, `#333333`.
- Unit switch input: `640px` wide, `48px` high, `12px 16px` padding, `2px solid #1F1F1F`.
- Unit switch action: link-style button, Gotham Rounded Bold, `16px`, `24px` line height, `#007485`.
- Use the unit switch input when one unit should be the default and the user can switch units, for example defaulting to acres with `Switch to hectares`.
- Radio option row height: `40px`.
- Radio input size: `40px` with `2px` dark border.
- Selected radio inner dot: `20px`, centred inside the radio.
- Radio focus state: `4px` dark border with `0 0 0 3px #FFDD00` focus ring.
- Radio input-to-label gap: `16px`.
- Radio label and hint text use Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Radio group label: Gotham Rounded Bold, `18px`, `24px` line height, `#333333`.
- Radio group width: `640px`; label/hint block width: `630px`; group gap: `16px`; options gap: `24px`.
- Radio group error state: `24px` left padding with `4px` red left bar in `#D43F46`; error text is bold `16px`, `24px` line height, `#D43F46`.
- Small radio variant: `32px` control and row height, `14px` label, `24px` line height.
- Radio hint variant height: `61px`.
- Radio conditional reveal panel: `640px` wide, `108px` high, `18px` left padding, `4px` left border in `#B1B4B6`, nested content width `582px`.
- Radio group vertical gap: `24px`.
- Checkbox option row height: `40px`.
- Checkbox input size: `40px` with `2px` dark border.
- Checkbox focus state: `4px` dark border with `0 0 0 3px #FFDD00` focus ring.
- Checkbox selected icon: `25px` by `20px`, `#1F1F1F`.
- Checkbox input-to-label gap: `16px`.
- Checkbox label and hint text use Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Small checkbox variant: `32px` control and row height, `17.5px` by `14px` selected icon, `14px` label, `24px` line height, `0 0 0 6px #FFDD00` focus ring.
- Disabled checkbox state: border and selected icon use `#E3E3E3`.
- Checkbox conditional reveal panel: `630px` wide, `75px` high, `18px` left padding, `4px` left border in `#B1B4B6`, nested content width `574px`.
- File upload drop zone width: `640px`.
- File upload drop zone minimum height: `172px`.
- File upload drop zone padding: `24px`.
- File upload drop zone gap: `16px`.
- File upload default border: `2px dashed #1F1F1F`.
- File upload hover state: `#F4F4F4` background with `3px dashed #1F1F1F`.
- File upload drag/drop state: `#F4F4F4` background with `3px solid #1F1F1F`.
- File upload focus state: `#F4F4F4` background with `3px solid #1F1F1F` and `0 0 0 3px #FFDD00`.
- File upload instruction text: Gotham Rounded Book, `20px`, `24px` line height, `#333333`.
- File upload browse button uses the medium primary NRW button: `40px` high, `8px 12px` padding, `#358728` background, `#26601C` hover.
- File upload selected-file table width: `min(672px, 100%)`; headings use H4 styling and rows use body text.
- Summary card width: `640px`.
- Summary card border: `1px solid #A1A1A1`.
- Summary card header: `56px` high, `#F4F4F4` background, `0 24px` padding.
- Summary card title: Gotham Rounded Bold, `18px`, `24px` line height, `#333333`.
- Summary card action link: Gotham Rounded Bold, `16px`, `24px` line height, `#007485`, right aligned.
- Summary card content uses two `320px` columns.
- Summary card rows are `56px` to `57px` high.
- Summary card key cells use Gotham Rounded Bold, `16px`, `24px` line height, `#333333`.
- Summary card value cells use Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Summary card row dividers use `2px solid #A1A1A1`.
- Three-column summary list width: `770px`.
- Three-column summary list columns: `256.67px` each.
- Three-column summary list rows: `57px` high.
- Three-column summary list key cells use Gotham Rounded Bold, `16px`, `24px` line height, `#333333`.
- Three-column summary list value cells use Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Three-column summary list action cells use Gotham Rounded Bold, `16px`, `24px` line height, `#007485`, right aligned.
- Three-column summary list row dividers use `2px solid #A1A1A1`.
- Primary and secondary form actions sit in a row with a `32px` gap.
- Form buttons are `48px` high with `12px 16px` padding and `4px` border radius.
- Footer feedback row height: `104px`.
- Use `work/nrw-prototype-components/components/footer.md` as the detailed source for footer layout, link row, divider, logo, and copyright rules.

### Focus And Interaction States

- All interactive elements must have visible focus states.
- Preserve keyboard navigation.
- Make buttons, links, radios, checkboxes, selects, tabs, accordions, and menus behave as users expect.
- Do not fake controls with static text.

## 6. Component Inventory

All core components come from the GOV.UK Design System. Use GOV.UK component guidance as the baseline for HTML structure, accessibility, interaction behaviour, validation behaviour, and when to use or avoid each component.

Apply NRW visual rules from this file on top of GOV.UK components:

- Gotham Rounded typography
- NRW colour tokens
- NRW header, footer, language toggle, sign-in, and page shell layout
- documented NRW spacing or layout differences
- bilingual Welsh and English service needs
- component text should generally use body weight, not bold, unless the approved NRW component variant shows otherwise

Do not redesign GOV.UK components unless the NRW Figma design system documents a specific variation.

| Component | GOV.UK source | Prototype notes |
| --- | --- | --- |
| Accordion | https://design-system.service.gov.uk/components/accordion/ | Use only when users need to show and hide related content; do not use for content all users must see or to split up a series of questions |
| Back link | https://design-system.service.gov.uk/components/back-link/ | Use for linear journeys |
| Breadcrumbs | https://design-system.service.gov.uk/components/breadcrumbs/ | Use for hierarchy, not step-by-step journeys |
| Button | https://design-system.service.gov.uk/components/button/ | Use GOV.UK behaviour, but apply the NRW button visual exception below |
| Character count | https://design-system.service.gov.uk/components/character-count/ | Use when text length matters to the service |
| Checkboxes | https://design-system.service.gov.uk/components/checkboxes/ | Use for multiple options |
| Cookie banner | https://design-system.service.gov.uk/components/cookie-banner/ | Use when the prototype needs cookie consent behaviour |
| Date input | https://design-system.service.gov.uk/components/date-input/ | Use separate day, month, and year fields |
| Details | https://design-system.service.gov.uk/components/details/ | Use for short optional supporting information |
| Error message | https://design-system.service.gov.uk/components/error-message/ | Place next to the field in error |
| Error summary | https://design-system.service.gov.uk/components/error-summary/ | Link to each invalid field |
| Fieldset | https://design-system.service.gov.uk/components/fieldset/ | Use to group related form controls |
| File upload | https://design-system.service.gov.uk/components/file-upload/ | Include selected, error, and success states where relevant |
| Footer | https://design-system.service.gov.uk/components/footer/ | Use GOV.UK behaviour with NRW visual footer treatment |
| Header | https://design-system.service.gov.uk/components/header/ | Use GOV.UK behaviour with NRW logo, language toggle, sign-in, and top nav treatment |
| Inset text | https://design-system.service.gov.uk/components/inset-text/ | Use for important supporting information, not warnings |
| Modal | `[NRW exception]` | GOV.UK does not provide a standard modal component; use the NRW modal exception below when a modal is explicitly needed |
| Notification banner | https://design-system.service.gov.uk/components/notification-banner/ | Use for status messages |
| Pagination | https://design-system.service.gov.uk/components/pagination/ | Use for long lists or record sets |
| Panel | https://design-system.service.gov.uk/components/panel/ | Use for confirmation pages |
| Password input | https://design-system.service.gov.uk/components/password-input/ | Use for authentication flows |
| Phase banner | https://design-system.service.gov.uk/components/phase-banner/ | Use when prototype status must be visible |
| Radios | https://design-system.service.gov.uk/components/radios/ | Use for one option from a list |
| Select | https://design-system.service.gov.uk/components/select/ | Avoid when radios are clearer |
| Service navigation | https://design-system.service.gov.uk/components/service-navigation/ | Use for persistent service sections |
| Skip link | https://design-system.service.gov.uk/components/skip-link/ | Include for keyboard users |
| Summary list | https://design-system.service.gov.uk/components/summary-list/ | Use on review pages; apply the NRW summary card styling below when using summary cards |
| Table | https://design-system.service.gov.uk/components/table/ | Use for comparison or records |
| Tabs | https://design-system.service.gov.uk/components/tabs/ | Use for related views, not journey steps |
| Tag | https://design-system.service.gov.uk/components/tag/ | Use GOV.UK guidance for status semantics, but apply the NRW badge visual exception below |
| Task list | https://design-system.service.gov.uk/components/task-list/ | Use for multi-part services |
| Text input | https://design-system.service.gov.uk/components/text-input/ | Include label, hint text, and error state; apply the NRW compact text input styling below |
| Textarea | https://design-system.service.gov.uk/components/textarea/ | Include character count if needed |
| Toast | `[NRW exception]` | GOV.UK does not provide toast notifications; use the NRW toast exception below for temporary dismissible messages |
| Warning text | https://design-system.service.gov.uk/components/warning-text/ | Use sparingly for important warnings |

### NRW Button Exception

NRW buttons differ visually from GOV.UK buttons. Use GOV.UK button guidance for semantics and behaviour, but apply these NRW button styles.

Button typography:

- Font family: Gotham Rounded.
- Font weight: Bold.
- Large button text: `18px`, `24px` line height.
- Medium button text: `16px`, `24px` line height.
- Small button text: `14px`, `24px` line height.
- Text and icon align to the bottom of the `24px` text line.

Button sizes:

| Size | Height | Padding | Gap | Icon |
| --- | --- | --- | --- | --- |
| Large | `48px` | `12px 16px` | `12px` | `24px` |
| Medium | `40px` | `8px 12px` | `12px` | `24px` |
| Small | `36px` | `6px 12px` | `8px` | `16px` |

Button types:

| Type | Default background | Border | Text and icon |
| --- | --- | --- | --- |
| Primary | `#358728` | none | `#FFFFFF` |
| Secondary | `#FFFFFF` | `2px solid #358728` | `#358728` |
| Tertiary | `#FFFFFF` | `2px solid #58595B` with inset shadow `0px -2px 0px #929191` | `#58595B` |
| Danger | `#D43F46` | none | `#FFFFFF` |

Button states:

- Primary hover: background `#26601C`, text and icon `#FFFFFF`.
- Secondary hover: background `#26601C`, text and icon `#FFFFFF`.
- Tertiary hover: background `#58595B`, text and icon `#FFFFFF`.
- Danger hover: background `#942C31` for large, `#55191C` for medium.
- Focus and pressed: background `#FFDD00`, text and icon `#0B0C0C`, shadow `0px 5px 0px #0B0C0C`.
- Loading: keep default background and overlay with `rgba(11, 27, 8, 0.9)` plus a `24px` loader.
- Border radius: `4px`.
- Use the chevron-right icon when the approved Figma button variant includes it.

### NRW Summary Card Styling

Use summary lists to summarise information, for example a user's responses at the end of a form. Summary cards are a variant within this component. Use summary cards to show multiple summary lists that describe the same type of thing, such as people, locations, activities, documents, or application parts. Card actions apply to the whole summary list.

Card structure:

- Width: `640px`.
- Border: `1px solid #A1A1A1`.
- Header row height: `56px`.
- Header background: `#F4F4F4`.
- Header padding: `0 24px`.
- Header inner content: `592px` wide, `16px 0` padding, `10px` gap.
- Title column: `296px` wide with `0 8px` padding.
- Action column: `296px` wide, right aligned.

Typography:

- Card title: Gotham Rounded Bold, `18px`, `24px` line height, `#333333`.
- Card action link: Gotham Rounded Bold, `16px`, `24px` line height, `#007485`.
- Summary key text: Gotham Rounded Bold, `16px`, `24px` line height, `#333333`.
- Summary value text: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.

Rows:

- Content area width: `640px`.
- Use two columns of `320px` on desktop.
- Row height: `56px` to `57px`.
- Left/key cells use `0 0 0 24px` outer padding and `16px 8px` inner padding.
- Right/value cells use `0 24px 0 0` outer padding and `16px 8px` inner padding.
- Row dividers use `2px solid #A1A1A1`.
- Use semantic `dl`, `dt`, and `dd` markup.

Three-column summary list variant:

- Use for rows that need a key, value, and row-level action link.
- Width: `770px`.
- Columns: three equal columns of `256.67px`.
- Row height: `57px`.
- Key cells use Gotham Rounded Bold, `16px`, `24px` line height, `#333333`.
- Value cells use Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Action cells use Gotham Rounded Bold, `16px`, `24px` line height, `#007485`, right aligned.
- Row dividers use `2px solid #A1A1A1`.

### NRW File Upload Styling

NRW file upload differs visually from the plain GOV.UK file upload. Use GOV.UK file upload guidance for semantics, labels, validation, file type constraints, and error messages, but apply the NRW upload area styling below.

Drop zone:

- Width: `640px`.
- Minimum height: `172px`.
- Padding: `24px`.
- Gap: `16px`.
- Background: `#FFFFFF`.
- Border: `2px dashed #1F1F1F`.
- Instruction text: `Drag and drop or`, Gotham Rounded Book, `20px`, `24px` line height, `#333333`.
- Browse button: medium primary NRW button, `126px` wide by `40px` high.

States:

- Hover: background `#F4F4F4`, border `3px dashed #1F1F1F`.
- Drag-over or file-drop: background `#F4F4F4`, border `3px solid #1F1F1F`.
- Focus: background `#F4F4F4`, border `3px solid #1F1F1F`, shadow `0 0 0 3px #FFDD00`.
- Button focus or pressed: background `#FFDD00`, text `#0B0C0C`, shadow `0 5px 0 #0B0C0C`.

Selected-file table:

- Width: `min(672px, 100%)`.
- Columns: `Filename`, `Size`, `Status`.
- Header top padding: `24px`.
- Header text: Gotham Rounded Bold, `16px`, `20px` line height, `#58595B`.
- Row top padding: `12px`.
- Row text: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Dividers: `#E3E3E3`.

### NRW Text Input Styling

Use GOV.UK text input guidance for labels, hints, error messages, autocomplete, input type, and validation behaviour. Apply the NRW compact input style where the Figma template shows the `Building blocks/Text` component.

- Width: `640px`.
- Height: `38px`.
- Padding: `8px 16px 8px 12px`.
- Background: `#FFFFFF`.
- Border: `2px solid #1F1F1F`.
- Text: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.
- Hint text: Gotham Rounded Book, `16px`, `24px` line height, `#333333`.

### NRW Badge Exception

NRW badges differ from the GOV.UK tag visual style. Use GOV.UK tag guidance for when a status badge is appropriate, but use the NRW badge dimensions and colours below.

Badge structure:

- Height: `25px`.
- Padding: `1px 8px 0px`.
- Border radius: `4px`.
- Text: Gotham Rounded bold, `16px`, `24px` line height.
- Use compact widths based on content rather than a fixed badge width.
- Positive badges use a solid background with white text, except yellow which uses body text.
- Negative badges use a light background with dark coloured text.

Badge colour variants:

| Variant | Background | Text |
| --- | --- | --- |
| Grey negative | `#E9E9EA` | `#58595B` |
| Grey positive | `#58595B` | `#FFFFFF` |
| Red negative | `#FBECED` | `#D43F46` |
| Red positive | `#D43F46` | `#FFFFFF` |
| Green negative | `#F0F5F4` | `#128300` |
| Green positive | `#128300` | `#FFFFFF` |
| Orange negative | `#FFF4ED` | `#D04716` |
| Orange positive | `#FF9447` | `#FFFFFF` |
| Yellow positive | `#FFDD00` | `#333333` |

### NRW Modal Exception

NRW modals differ from GOV.UK components because GOV.UK does not provide a standard modal component. Use modals only when the interaction genuinely needs an interruptive overlay, such as confirming a destructive action, showing a short focused task, or asking the user to make a decision before continuing.

Component set:

- Component set name: `Modals`.
- Figma component-set wrapper: `768px` wide, `1741px` high, `24px` padding, `24px` gap.

Shared modal shell:

- Dialog and login modal width: `670px`.
- Dialog modal height: `498px`.
- Login modal height: `584px`.
- Action modal width: `720px`.
- Action modal height: `563px`.
- Background: `#FFFFFF`.
- Shadow: `0px 8px 12px rgba(0, 0, 0, 0.2)`.
- Main content horizontal padding: `32px`.
- Close action row: `16px 16px 0px` padding, `40px` high, right aligned.
- Close link/icon colour: `#A1A1A1`.
- Modal heading: `36px` bold, `44px` line height, colour `#58595B`.
- Modal description: `18px`, `26px` line height for short intro copy.
- Body copy: `16px`, `24px` line height, colour `#333333`.

Dialog variant:

- Width: `670px`; height: `498px`.
- Heading area: `0px 32px`, `78px` high, `8px` heading gap.
- Information area: `0px 32px 40px`, `24px` gap.
- Inner content width: `606px`.
- Link list gap: `8px`.
- Footer action container: `32px 0px 0px` top padding, `16px` gap, right aligned.
- Secondary button: outlined green, `48px` high, `12px 16px` padding, `2px` border.
- Primary button: solid green, `48px` high, `12px 16px` padding.

Login variant:

- Width: `670px`; height: `584px`.
- Heading area: `0px 32px`, `88px` high.
- Information area: `0px 32px 40px`, `24px` gap.
- Text fields: `560px` wide, `80px` high, `8px` field gap.
- Text input box: `560px` wide, `48px` high, `12px 16px` padding, `2px solid #1F1F1F`.
- Primary action button: solid green, `48px` high, `12px 16px` padding.
- Supporting links use `16px` bold link text in `#007485`.

Action variant:

- Width: `720px`; height: `563px`.
- Heading content area: `80px` padding, `24px` gap, centred.
- Icon size: `56px`; warning icon colour: `#FF9447`.
- Heading and description max width: `560px`.
- Heading and description text align centre.
- Divider: `2px` high, `#E3E3E3`.
- Action footer: `40px` padding, `32px` gap, `120px` high, right aligned.
- Medium buttons: `40px` high, `8px 12px` padding, `16px` bold text.
- Grey secondary button: white background, `2px solid #58595B`, inset shadow `0px -2px 0px #929191`, text `#58595B`.
- Green secondary button: white background, `2px solid #358728`, inset shadow `0px -2px 0px #929191`, text `#358728`.
- Primary button: solid `#358728`, white text.

Notification inside action modal:

- Notification container: `720px` wide, `16px` padding.
- Banner: `688px` wide, `58px` high, `16px` padding, `16px` gap.
- Error banner background: `#FBECED`.
- Error icon colour: `#D43F46`.
- Banner radius: `4px`.
- Banner shadow: `0px 8px 12px rgba(0, 0, 0, 0.2)`.
- Banner heading: `18px` bold, `26px` line height, colour `#1F1F1F`.

Prototype behaviour requirements:

- Trap keyboard focus inside the modal while open.
- Move focus to the modal heading or first meaningful control when opened.
- Return focus to the triggering control when closed.
- Provide a visible close control unless the modal is a blocking confirmation.
- Close on `Esc` unless the modal contains a critical blocking decision.
- Prevent page scroll behind the modal.
- Use semantic dialog markup, including an accessible name.
- Include clear primary and secondary actions when a decision is required.
- Add an overlay behind the modal when implemented; if Figma overlay colour is not specified, use a subdued dark overlay and verify contrast and focus visibility.

### NRW Toast Exception

NRW toasts differ from GOV.UK notification banners. Use GOV.UK notification banners for prominent page-level messages that should remain in the page flow. Use NRW toasts for short, temporary, dismissible feedback after an action.

Toast structure:

- Width: `413px`.
- Height: `80px`.
- Padding: `16px`.
- Gap: `16px`.
- Border radius: `4px`.
- Icon size: `24px`.
- Content width: `301px`.
- Content height: `48px`.
- Heading: `16px` bold, `20px` line height, colour `#333333`.
- Supporting text: `14px`, `24px` line height, colour `#58595B`.
- Close icon: `24px`, colour `#A1A1A1`.
- Optional action links sit below the message content with `12px` gap and `0px 0px 4px` padding.

Toast variants:

| Variant | Background | Icon colour |
| --- | --- | --- |
| Success | `#F0F5F4` | `#128300` |
| Error | `#FBECED` | `#D43F46` |
| Info | `#E6F3F4` | `#349AC0` |
| Warning | `#FFF4ED` | `#FF9447` |

Toast behaviour:

- Place toasts in a consistent viewport position, usually top right for desktop unless the page template specifies otherwise.
- Keep toast text short enough to fit the `301px` content column.
- Do not use toasts for critical errors, validation summaries, legal notices, or information the user must retain.
- Provide a visible dismiss control.
- Do not rely on auto-dismiss alone; users must have enough time to read the message.
- Announce toast content to assistive technology using an appropriate live region.

## 7. Page Patterns

### Start Page

Use when a user begins a service.

Must include:

- service title
- short description
- eligibility or before-you-start information if needed
- primary start button
- support or alternative route where relevant

### External Sign-In Page

Use this pattern for external pages where the user is not signed in.

Must include:

- grey top navigation bar with logo on the left
- language toggle and sign-in action on the right
- aqua heading band with the page title in white
- centred `1020px` content container
- left-justified main content column of `640px`
- optional related links column of `316px`
- feedback link row above the footer, or inline feedback within the content column when the approved page template shows it there
- dark grey footer with green top accent bar

Layout notes:

- Keep the top navigation and heading band full width.
- Keep body content aligned to the centred container rather than the viewport edge.
- Use `40px` gaps between major columns and page sections.
- Use `16px` gaps inside text groups.
- Do not include hidden account, logout, menu, or decorative vector layers unless the prototype specifically needs those states.

### Question Page

Use when asking for one meaningful piece of information.

Must include:

- back link
- clear heading
- question information line under the heading where helpful
- one main input group
- continue button
- validation error state

Layout notes:

- Put information that explains the whole question directly under the question heading as supporting body copy, not as field-level hint text.
- Use a `16px` gap between the question heading and the supporting information line.
- Use field-level hint text only when the help belongs specifically to one input control, not to the whole question.
- Use a `24px` gap between the question text group and the form control.

### Task List Page

Use as the first page for multi-section application prototypes.

Must include:

- standard NRW top navigation, page heading band, and footer
- left-justified `640px` content column inside the `1020px` content wrapper
- H2 matching the service or application task
- short supporting copy where helpful
- grouped task sections using the NRW `Summary=Card, Width=Default` component
- task row links into the relevant journey screens
- status text for each row, such as `Not started` and `Completed`

Layout notes:

- Use the standard application template: `48px 16px` content padding.
- Use `56px` between the heading/supporting copy block and the task-list sections.
- Use `640px` wide summary cards for each task group.
- Section headers must use the NRW summary-card grey header row: `56px` high, `#F4F4F4`, `0 24px` padding, full-width `18px` bold title.
- Task rows must use semantic summary-list rows: `57px` high, `2px solid #A1A1A1` dividers, task link on the left, status on the right.

Behaviour notes:

- The task list is the first visible screen.
- Every page should include a `Go back to task list` link that returns to the task list.
- Update statuses from entered answers where possible.

### Checkbox Confirmation Page

Use near the end of a journey when users must acknowledge important privacy, declaration, or legal information before continuing.

Must include:

- standard NRW top navigation, page heading band, and footer
- left-justified `640px` content column
- H2 page question or statement heading
- body copy directly under the heading
- one required checkbox using the NRW checkbox component
- standard Back and Save and continue buttons
- validation error state when the checkbox is not selected

Layout notes:

- Use the standard application question template spacing.
- Keep the explanatory body copy above the checkbox.
- Use body-weight checkbox labels.
- Use links with `target="_blank"` and visible “opens in a new tab” text when linking to external or supporting notices.

Behaviour notes:

- Save and continue validates the checkbox.
- Back returns to the previous journey step with entered answers preserved where possible.

### Long Form Question Set Page

Use when a service page needs more than one related question in the same step, such as technical screening, eligibility, or annex-style forms.

Must include:

- standard NRW top navigation and aqua page heading band
- `1200px` content wrapper with `48px 16px` padding
- one or more `770px` question blocks
- question heading, supporting body copy where needed, then the form control
- GOV.UK radio component behaviour for single-choice questions
- selected, unselected, focus, and error states for radio groups
- secondary back button and primary continue button
- feedback link row and standard footer

Layout notes:

- Stack question blocks vertically with a `32px` gap between major blocks.
- Keep each question block at `770px` wide on desktop.
- Use `24px` gap between the question text area and radio group.
- Use `16px` gap between a question heading and its supporting body text.
- Put information that explains the whole question directly under the question heading as supporting body copy. Do not put whole-question information into a field hint.
- Use `24px` vertical gap between radio options.
- Keep radio labels at `16px` with `24px` line height.
- Use a `40px` radio target with a `20px` selected dot.
- Place back and continue actions in a row, with back first and continue second.
- Use the outlined secondary button for back and the green primary button for continue.
- Do not include hidden radio options, hidden reveal panels, or hidden question blocks unless the prototype specifically needs branching behaviour.

### Multiple Questions With Dependent Follow-Up

Use when a yes/no or single-choice answer creates a follow-up question on the same page. For example, if a user says an application should be confidential, ask why as a second question block rather than as a small indented conditional reveal.

Must include:

- standard NRW top navigation and aqua page heading band
- `1020px` content wrapper with `48px 16px` padding
- `640px` content column
- first question block with heading, supporting body copy, and radio group
- second question block for the dependent follow-up when required
- secondary back button and primary continue button after the full question set
- feedback link row and standard footer

Layout notes:

- Use this pattern instead of an indented conditional reveal when the follow-up is a meaningful question with its own heading and explanatory body copy.
- Each follow-up must be a peer question block in the same column, not nested under the triggering radio option.
- Stack the question blocks in a `640px` column with `56px` between blocks.
- Each question block uses a `24px` gap between the heading/body copy group and its form control.
- Use `16px` between the question heading and supporting body copy.
- Put information that explains the whole question directly under the question heading as supporting body copy. Field-level hints are only for help that belongs to one specific control.
- When a progressive question has supporting body copy, group the heading and body copy together before the form control.
- Question headings use H2 styling: `30px` bold, `37px` line height, colour `#58595B`.
- Supporting body copy is `16px`, `24px` line height, colour `#333333`.
- The radio group is `640px` wide with `24px` vertical gap between options.
- Radio rows use a `40px` target, `16px` gap between input and label, and `456px` label content width.
- The dependent text area is `640px` wide and `180px` high.
- Text area padding is `12px 16px`; border is `2px solid #1F1F1F`.
- Use a `24px` helper or hint row below the text area when needed.
- Button group uses a `303px` container, `24px` vertical gap, and a `16px` gap between back and continue buttons.
- Back button width: `80px`; continue button width: `207px`; both are `48px` high with `12px 16px` padding.

Behaviour notes:

- If the answer is `Yes`, reveal or navigate to the second question block asking why.
- If the answer is `No`, do not show the follow-up question.
- When the follow-up question is shown, validate it as its own required question.
- Avoid placing a large text area inside a GOV.UK-style indented conditional reveal for this pattern.

### Add To A List

Use when users need to add similar information many times, check what they have added, and add more if needed.

Follow the MOJ Add to a list pattern for repeated journey items such as fish species, people, locations, or documents. Source: `https://design-patterns.service.justice.gov.uk/patterns/add-to-a-list/`.

If users only need to add information a couple of times, consider the MOJ Add another component instead.

Must include:

- standard NRW top navigation and aqua page heading band
- `1020px` content wrapper with `48px 16px` padding
- left-justified `640px` content column
- a GOV.UK-style question page for one item
- a progressive added-items state after the user adds an item
- a compact summary list on the added-items state
- a Yes/No radio question asking whether the user needs to add another item
- secondary back button and primary continue button
- validation error state for each required field on the item page
- validation error state for the Yes/No add-another question

Layout notes:

- Stack item questions in a `640px` column.
- Show the saved-item summary in the progressive added-items state.
- Use a compact `640px` summary list for saved items unless a separate check-answer page has been requested.
- Keep field labels at body size unless they are the main question heading.
- Use the standard primary `Save and continue` button to validate and add the first item.
- Use radios for the add-another decision after at least one item has been added.
- Change and remove links may be added to summary items when those journeys are defined.
- If a remove link is added, ask the user to confirm before removing the item.

Behaviour notes:

- Ask for one item at a time.
- Save and continue on the item entry state validates and saves the current item, updates the summary list, clears the fields, and shows the progressive added-items state.
- Save and continue on the added-items state validates the Yes/No radio answer.
- If the user answers `Yes`, return to a blank item question page.
- If the user answers `No`, continue to the next question.
- If the user changes a saved item, move that item back into the active fields and remove it from the saved summary until it is added again.
- If one field controls another field in the item question page, hide and clear the dependent field when it no longer applies.

Fish add-to-a-list variant:

- Use a `56px` gap between the main heading section and the fish questions.
- Use a `56px` gap between fish question blocks.
- Use a `24px` gap between each question text group and its control.
- Use a `16px` gap between a question heading and its supporting information line.
- Use full-width `640px` by `48px` inputs and selects for fish species, number, length, and weight.
- For length/weight, default to length and use a link-style switch action rather than exposing both controls at once.
- The first state uses the standard primary `Save and continue` button. Do not add a separate `Add fish` button.
- The added-fish state uses the heading `You have added X type(s) of fish`, a compact summary list with Change and Remove actions, and the question `Do you need to add another type of fish?`.

### Check Answers Page

Use before submission.

Must include:

- summary list of answers
- change links with specific accessible labels
- declaration or confirmation copy when needed
- submit button

### Confirmation Page

Use after successful submission.

Must include:

- confirmation panel
- reference number where realistic
- what happens next
- contact or support route
- link back to relevant service area

### Error And Problem Pages

Use for service failure, not found, or unavailable states.

Must include:

- plain explanation
- what the user can do next
- support route where needed
- no blame placed on the user

## 8. Content Rules

- Write in plain English.
- Use active voice.
- Start with the user need.
- Put important information before the action.
- Use specific button text when the action is specific.
- Avoid internal policy, delivery, or system language in the interface.
- Treat Welsh and English content as equal parts of the service.
- Plan bilingual content at the same time as the journey, not as a translation step at the end.
- Use vocabulary that matches how users talk about the service.
- Do not include real personal data in prototypes.

## 9. Accessibility Rules

Every prototype should be usable with:

- keyboard only
- screen reader-friendly labels and structure
- visible focus states
- semantic headings in order
- clear error summaries and field-level errors
- sufficient colour contrast
- responsive layouts at mobile and desktop sizes

For research prototypes, include accessibility-critical states even when the prototype is not production code.

Use WCAG 2.2 Level AA as the minimum accessibility target for digital service prototypes unless the project has a stricter internal standard.

## 10. Interaction Rules

Define the expected behaviour before building.

| Interaction | Prototype expectation |
| --- | --- |
| Form submission | Validate required fields and move to the next page |
| Back link | Return to the previous step with entered data preserved where possible |
| Change link | Return to the original question and then back to check answers |
| Small conditional reveal | Show and hide short related fields based on selection |
| Substantial dependent question | Show as a separate full question block in the same `640px` column, not as an indented conditional panel |
| Save and return | Include only if part of the tested flow |
| Search or filter | Use realistic sample data and empty states |
| Upload | Include file selected, error, and success states where relevant |
| Timeout | Include only for authentication or secure service flows |

## 11. Data And Content Fixtures

Use safe, realistic data.

- People: use fictional names.
- Addresses: use fictional or clearly sample addresses.
- Reference numbers: use fake but plausible formats.
- Dates: use realistic current or near-future examples.
- Statuses: use project-approved labels.
- Empty states: explain what the user can do next.

Do not use real user data, customer records, private case details, credentials, or policy-sensitive material.

## 12. Quality Checklist Before Sharing

Before handing over a prototype, check:

- It matches the Figma source and this file.
- It uses GOV.UK-like components and patterns unless documented otherwise.
- It supports the Digital Service Standard for Wales where relevant.
- Welsh and English language needs have been considered from the start.
- The journey has been checked for assisted digital, non-digital, and joined-up channel needs where relevant.
- The main task can be completed.
- Back links and change links work.
- Validation errors are visible and useful.
- Keyboard focus is visible.
- WCAG 2.2 Level AA needs have been considered.
- Mobile and desktop layouts do not overlap or clip text.
- Content is realistic, plain, and service-specific.
- No real personal data is included.
- Any assumptions are documented outside the visible UI.

## 13. Codex Build Instructions

When Codex builds from this file:

- Read this file before making UI decisions.
- Ask for missing Figma links, screenshots, or component references when visual fidelity matters.
- Prefer GOV.UK Frontend or GOV.UK Prototype Kit patterns for GOV.UK-like services.
- Use GOV.UK Prototype Kit as the default build stack.
- Use the project Figma components as the source of truth when they differ from GOV.UK.
- Build the requested task flow directly.
- Include functional form states and navigation for the requested fidelity.
- Verify the prototype at mobile and desktop sizes before handing it over.
- Check the prototype against the Digital Service Standard for Wales, especially user needs, bilingual content, accessibility, joined-up journeys, privacy/security, and evidence for decisions.


## 14. Useful References

- GOV.UK Design System: https://design-system.service.gov.uk/
- GOV.UK Design System components: https://design-system.service.gov.uk/components/
- GOV.UK Design System patterns: https://design-system.service.gov.uk/patterns/
- GOV.UK Prototype Kit: https://prototype-kit.service.gov.uk/docs/
- Digital Service Standard for Wales: https://digitalpublicservices.gov.wales/guidance-and-standards/digital-service-standard-wales
- Digital Service Standard for Wales - Meet user needs: https://digitalpublicservices.gov.wales/guidance-and-standards/digital-service-standard-wales/meet-user-needs
- Digital Service Standard for Wales - Create digital teams: https://digitalpublicservices.gov.wales/guidance-and-standards/digital-service-standard-wales/create-digital-teams
