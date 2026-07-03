# Freshwater Fish Flows Prototype Plan

Working plan for a real prototype. Screens and flow rules should only be added when they are provided or explicitly approved.

Use `outputs/codex-prototype-design-system.md` and `work/nrw-prototype-components/` as the design source of truth.

## Confirmed Scope

- Prototype name: `Freshwater Fish Flows`
- Purpose: users apply for a licence or permit and review their answers at the end.
- Interactivity: full working journey with branching and validation.
- Visual system: NRW design system components, with GOV.UK fallback where NRW is incomplete.

## Build Rule

Do not invent screens, branches, eligibility rules, question wording, options, evidence requirements, or review-page content.

For each screen, define the content and behaviour first, then add it to the prototype.

## Screen Register

| ID | Screen | Source or approval | Status | Notes |
| --- | --- | --- | --- | --- |
| 00 | Landing screen | User provided on 2026-06-26; opening screen updated on 2026-07-02 | Built | First page of the prototype. Uses the NRW page shell and presents three category sections: `Marine licensing`, `Freshwater fish permits`, and `Land access`. Only `Freshwater fish permits` links into the working journey; the other two categories are visible but inactive. |
| 01 | Applications | User provided on 2026-07-02 | Built | Opens after `Freshwater fish permits` is selected. Uses two full-width four-column lists. `Applications in progress` contains `Draft` and `Submitted` rows. `Permits` contains `Active`, `Expired`, and `Rejected` rows. All `Continue`, `View`, and `Amend` actions open the completed application task list. |
| 02 | Completed application task list | User provided on 2026-07-02 | Built | Opens from all `Continue`, `View`, and `Amend` actions on the applications dashboard. Uses grouped summary cards for `Application details`, `Fish and environment`, and `Review and submit`, with all rows marked `Completed`. |
| 03 | Who is the licence for? | User provided on 2026-07-03 | Built | New first journey screen before the task question. Radio options with hint text: `A public body` with hint `For example - a council`, `A charity`, `A company`, and `An individual` with hint `As an individual acting independently`. Back returns to the current task-list view. Save and continue validates required answer and goes to Screen 04. |
| 04 | Are you applying on behalf of someone else? | User provided on 2026-07-03 | Built | Second contact-details screen before the task question. Radio options: `Yes` with hint `For example, you are an agent, consultant or contractor` and `No` with hint `For example, you are applying for yourself, or a company you work for or own`. Back returns to Screen 03. Save and continue validates required answer and goes to Screen 05. |
| 05 | Contact details and contact language | User provided on 2026-07-03 | Built | Conditional screen shown only when the user selects `Individual` on Screen 03 and `No` on Screen 04. Collects `Name`, `Email address`, `Phone number`, `Address`, and `Contact language`. Back returns to Screen 04. Save and continue validates required answers and goes to Screen 06. |
| 06 | Which task are you planning on completing? | User provided on 2026-06-25; exact Template layout supplied on 2026-06-26; left-justified body content clarified on 2026-06-26 | Built | Main header: `Apply for permission to stock, remove and supply fish`. Uses long 182px NRW page heading, left-justified 640px content column, visible body copy, radio options: `Stocking fish`, `Supplying fish`, `Removing fish`, Back and Save and continue buttons, task-list link, inline feedback link, and NRW footer link set. Back returns to Screen 05 when the conditional contact-details branch is active, otherwise Screen 04. Save and continue validates required answer. All three task routes branch to Screen 07. |
| 07 | What is the name of the water? | User provided on 2026-06-25; split-screen GOV.UK pattern agreed on 2026-06-25; shared route confirmed on 2026-06-26 | Built | Shared by supply, stocking, and removal routes. Single-question page using question heading only. Text input label is visually hidden. Required validation. Back returns to Screen 06. Save and continue goes to Screen 08. |
| 08 | What type of water is it? | User provided on 2026-06-25; split-screen GOV.UK pattern agreed on 2026-06-25; shared route confirmed on 2026-06-26; progressive stillwater questions provided on 2026-06-26 | Built | Shared by supply, stocking, and removal routes. Uses progressive question blocks on the same screen. Asks for water type with options `Canal`, `River`, `Stillwater`. If `Stillwater` is selected, reveals a separate CEFAS registration number question block. If the selected task was `Supplying fish`, also reveals a separate landlocked/on line question block. Back returns to Screen 07. Save and continue goes to Screen 09. |
| 09 | What is the nearest town/city of your proposed activity? | User provided on 2026-06-26; question information placement clarified on 2026-06-26 | Built | Shared by supply, stocking, and removal routes. Text input question with question information line: `This will appear on your application form`. Back returns to Screen 08. Save and continue goes to Screen 10. |
| 10 | Provide a National Grid Reference / Provide a what3words (optional) | User provided on 2026-06-26 | Built | Shared by supply, stocking, and removal routes. Two text input question blocks on the same page. National Grid Reference is required. what3words is optional. Back returns to Screen 09. Save and continue goes to Screen 11. |
| 11 | Are any of the fish a non-native species? | User provided on 2026-06-26 | Built | Shared by supply, stocking, and removal routes. Radio options: `Yes`, `No`, `Unknown`. Required validation. Back returns to Screen 10. Save and continue goes to Screen 12. |
| 12 | Are there any crayfish present? | User provided on 2026-06-26 | Built | Shared by supply, stocking, and removal routes. Radio options: `Yes`, `No`, `Unknown`. Required validation. Back returns to Screen 11. Save and continue goes to Screen 13. |
| 13 | Fish | User provided on 2026-06-26; updated to follow supplied progressive disclosure screenshots on 2026-06-26 | Built | Shared by supply, stocking, and removal routes. Progressive add-to-list journey. First state asks for one fish species and uses the standard `Save and continue` button to add it. Added state shows `You have added X type(s) of fish`, a compact list with Change and Remove links, and asks `Do you need to add another type of fish?`. Back returns to Screen 12. If the user answers `No`, Save and continue goes to Screen 14. |
| 14 | How we use your personal data | User provided on 2026-06-26 | Built | Shared by supply, stocking, and removal routes. Content page with required checkbox: `I have read and understood this information`. Back returns to Screen 13 added-fish state. Save and continue goes to Screen 15. |
| 15 | Declaration | User provided on 2026-06-26 | Built | Shared by supply, stocking, and removal routes. Declaration page with required checkbox: `To the best of my knowledge and belief, the information I have given is correct`. Back returns to Screen 14. Save and continue reaches the current prototype holding message. |

## Screen Definition Template

Use this template for each screen before building it.

### Screen ID

TBD

### Page Heading

TBD

### Question Or Content

TBD

### Component Pattern

TBD

Examples:

- radio question
- checkbox question
- text input
- textarea
- file upload
- summary card
- check answers
- confirmation

### Options Or Fields

TBD

### Validation

TBD

### Branching

TBD

### Back Link Or Back Button Behaviour

TBD

### Continue Or Submit Behaviour

TBD

## Confirmed Components Available

- NRW top nav
- NRW page heading
- NRW footer
- NRW buttons
- NRW radios
- NRW checkboxes
- NRW text input
- NRW textarea
- NRW file upload
- NRW summary card and summary list
- GOV.UK error summary and field-level errors with NRW styling

## GOV.UK Fallback Rules

Use GOV.UK behaviour and accessibility guidance when NRW has no specific pattern yet. Apply NRW typography, colours, page shell, header, footer, and known component styling on top.

## Defined Screens

### Screen 00

### Page Heading

Apply for permission to stock, remove and supply fish

### Question Or Content

Apply for permission to stock, remove and supply fish

Supporting copy:

Complete each section of the application.

### Component Pattern

Landing screen using the NRW page shell and grouped category links.

Uses the supplied page template layout:

- `1020px` content width container
- `48px 16px` content padding
- left-justified `640px` content column
- grouped category sections with heading, supporting copy, section link, and status text
- `56px` gap between the intro text and landing sections

### Options Or Fields

- Marine licensing
- Freshwater fish permits
- Land access

### Validation

None.

### Branching

Each task-list row links to its relevant screen.

All journey pages include a `Go back to task list` link that returns to this screen.

### Back Link Or Back Button Behaviour

Not applicable.

### Continue Or Submit Behaviour

Not applicable.

### Screen 01

### Page Heading

Apply for permission to stock, remove and supply fish

### Question Or Content

Which task are you planning on completing?

Body copy:

You need to apply for consent to:

- remove fish from your fishery other than by rod and line
- introduce fish into your fishery (a site permit)
- supply fish to fisheries, or move fish between sites (a supplier permit)

These permits are free.

### Component Pattern

Radio question.

Uses the approved `Template` Figma export:

- long NRW page heading variant
- supplied Template layout
- 1020px content width container
- 988px column row
- left-justified 640px content container
- 16px gap between question heading and supporting body copy
- 24px gap between question text and radio group
- 24px gap between radio options
- 32px gap between column container and button group
- Back and Save and continue action row inside a 303px button group
- 24px gap between action row and Go back to task list link
- inline page feedback link

### Options Or Fields

- Stocking fish
- Supplying fish
- Removing fish

### Validation

User must select one option before continuing.

### Branching

Not yet defined.

### Back Link Or Back Button Behaviour

Back button is shown because it appears in the approved template. No previous screen has been defined yet.

The `Go back to task list` link is shown because it appears in the approved screenshot.

### Continue Or Submit Behaviour

Save and continue saves the selected task.

If the user selects `Stocking fish`, `Supplying fish`, or `Removing fish`, continue to Screen 02.

### Screen 02

### Page Heading

Apply for permission to stock, remove and supply fish

### Question Or Content

What is the name of the water?

### Component Pattern

Text input question.

Uses the supplied Template layout with NRW typography, controls, buttons, page heading, and footer. This is a single-question page, so there is no separate visible section heading.

### Options Or Fields

- Name of the water

The field label is visually hidden because the question heading is the visible label.

### Validation

User must enter the name of the water.

### Branching

All task routes continue to Screen 03.

### Back Link Or Back Button Behaviour

Back returns to Screen 01.

### Continue Or Submit Behaviour

Save and continue validates the water name and moves to Screen 03.

### Screen 03

### Page Heading

Apply for permission to stock, remove and supply fish

### Question Or Content

What type of water is it?

### Component Pattern

Radio question.

Uses the supplied Template layout with NRW typography, controls, buttons, page heading, and footer. This is a single-question page, so there is no separate visible section heading.

### Options Or Fields

- Canal
- River
- Stillwater

Progressive question block shown when `Stillwater` is selected:

- What is your CEFAS registration number?

Additional progressive question block shown only when the selected task is `Stocking fish`:

- What is the size of the water?
  - Size input defaults to acres
  - Link-style button switches the input unit between acres and hectares

Additional progressive question block shown only when the selected task is `Supplying fish`:

- Is the water landlocked or on line?
  - Yes
  - No

### Validation

User must select the type of water.

If `Stillwater` is selected, user must enter a CEFAS registration number.

If `Stillwater` is selected and the selected task is `Stocking fish`, user must enter the size of the water. Acres is the default unit, with a link-style button to switch to hectares.

If `Stillwater` is selected and the selected task is `Supplying fish`, user must answer whether the water is landlocked or on line.

### Branching

Not yet defined.

### Back Link Or Back Button Behaviour

Back returns to Screen 02.

### Continue Or Submit Behaviour

Save and continue validates the water type and moves to Screen 04.

### Screen 04

### Page Heading

Apply for permission to stock, remove and supply fish

### Question Or Content

What is the nearest town/city of your proposed activity?

Question information line:

This will appear on your application form

### Component Pattern

Text input question.

Uses the supplied Template layout with NRW typography, controls, buttons, page heading, and footer. This is a single-question page, so there is no separate visible section heading.

### Options Or Fields

- Nearest town/city

The field label is visually hidden because the question heading is the visible label.

### Validation

User must enter the nearest town or city of the proposed activity.

### Branching

All task routes continue through this screen.

### Back Link Or Back Button Behaviour

Back returns to Screen 03.

### Continue Or Submit Behaviour

Save and continue validates the nearest town/city and moves to Screen 05.

### Screen 05

### Page Heading

Apply for permission to stock, remove and supply fish

### Question Or Content

Provide a National Grid Reference

Question information line:

You can search for your water's National Grid Reference on UK Grid Reference Finder

Provide a what3words (optional)

Question information line:

This will help us locate your body of water more accurately. You can search for it on what3words

### Component Pattern

Multiple text input questions on one page.

Uses the supplied Template layout with NRW typography, controls, buttons, page heading, and footer. The question information sits under each question heading as supporting body copy, not as field-level hint text.

### Options Or Fields

- National Grid Reference
- what3words

Field labels are visually hidden because each question heading is the visible label.

### Validation

User must enter a National Grid Reference.

what3words is optional.

### Branching

All task routes continue through this screen.

### Back Link Or Back Button Behaviour

Back returns to Screen 04.

### Continue Or Submit Behaviour

Save and continue validates the National Grid Reference and moves to Screen 06.

### Screen 06

### Page Heading

Apply for permission to stock, remove and supply fish

### Question Or Content

Are any of the fish a non-native species?

### Component Pattern

Radio question.

Uses the supplied Template layout with NRW typography, controls, buttons, page heading, and footer. This is a single-question page, so there is no separate visible section heading.

### Options Or Fields

- Yes
- No
- Unknown

### Validation

User must select one option.

### Branching

All task routes continue through this screen.

### Back Link Or Back Button Behaviour

Back returns to Screen 05.

### Continue Or Submit Behaviour

Save and continue validates the answer and moves to Screen 07.

### Screen 07

### Page Heading

Apply for permission to stock, remove and supply fish

### Question Or Content

Are there any crayfish present?

### Component Pattern

Radio question.

Uses the supplied Template layout with NRW typography, controls, buttons, page heading, and footer. This is a single-question page, so there is no separate visible section heading.

### Options Or Fields

- Yes
- No
- Unknown

### Validation

User must select one option.

### Branching

All task routes continue through this screen.

### Back Link Or Back Button Behaviour

Back returns to Screen 06.

### Continue Or Submit Behaviour

Save and continue validates the answer and moves to Screen 08.

### Screen 08

### Page Heading

Apply for permission to stock, remove and supply fish

### Question Or Content

Fish

Question information line:

Add in fish one species at a time

### Component Pattern

Add to a list.

Uses the MOJ Add to a list principle adapted to the supplied NRW progressive disclosure layout: ask for one fish entry at a time, use `Save and continue` to save the current fish, then show the added-fish state with a compact list and a Yes/No question asking whether another type of fish is needed. Source: `https://design-patterns.service.justice.gov.uk/patterns/add-to-a-list/`.

Uses the supplied fish layout spacing:

- 40px between the main heading section and the fish questions stack
- 56px between fish question blocks
- 24px between each question text group and its control
- 16px between a question heading and its supporting information line
- no extra default H2 margin inside the fish heading section
- 24px between the length/weight label and its input

### Options Or Fields

Fish entry state includes:

- Fish species
- Number of fish
  - 1-10
  - 10-20
  - 20-50
  - 50-100
  - 100+
- Length or weight

The length or weight section includes this question information line:

Please provide an estimation of the average length or weight of each fish

Default to `Length in cm` with a `Switch to weight` link.

If the user switches to weight, show `Weight in kg` with a `Switch to size` link.

### Validation

On the fish details page, user must enter:

- species
- number of fish
- whether they are providing length or weight
- length in cm, if length is selected
- weight in kg, if weight is selected

### Branching

All task routes continue through this screen.

After the user adds a fish, show the added-fish state:

- Heading: `You have added 1 type of fish` or `You have added X types of fish`
- Compact list row for each fish: species, number and length/weight, `Change`, `Remove`
- Question: `Do you need to add another type of fish?`
- Options: `Yes`, `No`

`Change` moves that fish back into the fields for editing. `Remove` removes the fish from the list.

### Back Link Or Back Button Behaviour

Back returns to Screen 07.

### Continue Or Submit Behaviour

On the fish entry state, Save and continue validates the current fish entry, adds it to the summary list, clears the fields, and shows the added-fish state.

On the added-fish state, Save and continue validates the Yes/No answer. If `Yes`, return to a blank fish entry state. If `No`, continue to Screen 09.

### Screen 09

### Page Heading

Apply for permission to stock, remove and supply fish

### Question Or Content

How we use your personal data

Body copy:

We’ll use the information you provide in line with UK data protection laws.

For more about how we collect, store and use your data, read our privacy notice (opens in a new tab).

### Component Pattern

Content page with required checkbox confirmation.

### Options Or Fields

- I have read and understood this information

### Validation

User must tick the checkbox to continue.

### Back Link Or Back Button Behaviour

Back returns to Screen 08 added-fish state.

### Continue Or Submit Behaviour

Save and continue validates the checkbox and moves to Screen 10.

### Screen 10

### Page Heading

Apply for permission to stock, remove and supply fish

### Question Or Content

Declaration

Body copy:

If you give any information which is incomplete or inaccurate:

- we will return your application; and/or
- we will not grant consent.

### Component Pattern

Declaration page with required checkbox confirmation.

### Options Or Fields

- To the best of my knowledge and belief, the information I have given is correct

### Validation

User must tick the checkbox to continue.

### Back Link Or Back Button Behaviour

Back returns to Screen 09.

### Continue Or Submit Behaviour

Save and continue validates the checkbox and reaches the current prototype holding message.
