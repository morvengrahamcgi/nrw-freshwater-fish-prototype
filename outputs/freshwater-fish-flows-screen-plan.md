# Freshwater Fish Flows Prototype Plan

Current source-of-truth plan for the built freshwater fish prototype.

Use this file together with:

- `outputs/codex-prototype-design-system.md`
- `outputs/design-agent-brief.md`
- `work/nrw-prototype-components/`
- `work/freshwater-fish-flows-prototype/index.html`

## Confirmed Scope

- Prototype name: `Freshwater Fish Flows`
- Purpose: let users move from a freshwater fish service landing screen into an applications dashboard, then into a permit journey and a review flow.
- Interactivity: full working HTML prototype with branching, validation, and back-button behaviour.
- Visual system: NRW design system components and layouts, with GOV.UK behaviour as fallback where NRW guidance is silent.

## Build Rule

Do not invent screens, branches, question wording, options, evidence requirements, or review-page content.

When new screenshots, Figma exports, or approved rules are provided, update this file so it stays aligned with the built prototype.

## Live Journey Summary

The prototype currently behaves like this:

1. `Select a service`
2. `Applications in progress / Permits`
3. `Are you applying on behalf of someone else?`
4. Conditional `Licence holder details`
5. `Which task are you planning on completing?`
6. Water, location, environment, fish, privacy, and declaration screens
7. `Check your answers before submitting your application`

## Branching Rules

- Only `Freshwater fish permits` is active on the landing screen.
- The applications dashboard includes five visible states:
  - `Draft`
  - `Submitted`
  - `Active`
  - `Expired`
  - `Rejected`
- `Draft` and `Submitted` sit under `Applications in progress`.
- `Active`, `Expired`, and `Rejected` sit under `Permits`.
- `Continue`, `View`, and `Amend` all open the completed application review screen.
- `Apply for a new permit` opens the new permit journey at `Are you applying on behalf of someone else?`
- The journey now skips the old `Who is the licence for?` screen and goes straight to the contractor question.
- After `Are you applying on behalf of someone else?`, always show a contact-details screen.
- If the user answers `Yes`, show the contractor version with contractor-specific heading and `Company name`.
- If the user answers `No`, show the existing `Licence holder details` version.

## Screen Register

| ID | Screen | Status | Notes |
| --- | --- | --- | --- |
| 00 | Service landing | Built | Uses the NRW page shell and three category sections: `Marine licensing`, `Freshwater fish permits`, and `Land access`. Only `Freshwater fish permits` is active. |
| 01 | Applications dashboard | Built | Opens after `Freshwater fish permits` is selected. Has `Applications in progress` and `Permits` sections, each using four-column application rows: `Water name`, `Case number`, `Status`, `Actions`. Includes `Apply for a new permit` at the bottom. |
| 02 | Check your answers before submitting your application | Built | Opens from `Continue`, `View`, and `Amend`. Uses NRW summary cards for `Licence holder details`, `Permit`, `Location`, `Fish`, `Privacy notice`, and `Declaration`. Bottom actions are `Back` and `Complete`. |
| 03 | Are you applying on behalf of someone else? | Built | Radio question with `Yes` and `No`, both with hint text. This is now the first screen in the new-permit journey. |
| 04 | Contact details | Built | Shared contact-details step shown after Screen 03. If the user answers `Yes`, this becomes `Your contact details - as the agent, consultant or contractor` and includes `Company name` after `Phone number`. If the user answers `No`, it uses the existing `Licence holder details` version. |
| 05 | Which task are you planning on completing? | Built | Radio question with `Stocking fish`, `Supplying fish`, `Removing fish`. Back returns to Screen 04 when the contact-details branch is present, otherwise Screen 03. |
| 06 | What is the name of the water? | Built | Single text-input question. |
| 07 | What type of water is it? | Built | Radio question with `Canal`, `River`, `Stillwater`. `Stillwater` reveals `What is your CEFAS registration number?`. `Stillwater` plus `Stocking fish` also reveals `What is the size of the water?`. `Stillwater` plus `Supplying fish` also reveals `Is the water landlocked or on line?` |
| 08 | What is the nearest town/city of your proposed activity? | Built | Text input question with the supporting line `This will appear on your application form`. |
| 09 | Provide a National Grid Reference / Provide a what3words (optional) | Built | Two-question page. National Grid Reference is required. what3words is optional. |
| 10 | Are any of the fish a non-native species? | Built | Radio question with `Yes`, `No`, `Unknown`. |
| 11 | Are there any crayfish present? | Built | Radio question with `Yes`, `No`, `Unknown`. |
| 12 | Fish | Built | Progressive add-to-list page. Starts with one fish-entry state, then moves to an added-fish summary state with `Change`, `Remove`, and `Do you need to add another type of fish?` |
| 13 | How we use your personal data | Built | Checkbox confirmation page with `I have read and understood this information`. |
| 14 | Declaration | Built | Checkbox confirmation page with `To the best of my knowledge and belief, the information I have given is correct`. |

## Screen Notes

### Screen 00: Service landing

- Main page heading: `Freshwater fish applications, licenses and permits`
- H2 inside the content column: `Select a service`
- Shows three visible service groups.
- `Marine licensing` and `Land access` are intentionally inactive.

### Screen 01: Applications dashboard

- Uses two visible sections:
  - `Applications in progress`
  - `Permits`
- Button at the bottom:
  - `Apply for a new permit`
- In-progress actions:
  - `Continue`
  - `Delete`
- Permit actions:
  - `View`
  - `Amend`

### Screen 02: Check your answers

- Main heading:
  - `Check your answers before submitting your application`
- Summary card groups:
  - `Licence holder details`
  - `Permit`
  - `Location`
  - `Fish`
  - `Privacy notice`
  - `Declaration`
- Primary bottom action:
  - `Complete`
- Secondary bottom action:
  - `Back`
- Change links route back into the relevant earlier screen.

### Screen 03: Are you applying on behalf of someone else?

- Options:
  - `Yes`
  - `No`
- Hint text:
  - `Yes`: `For example, you are an agent, consultant or contractor`
  - `No`: `For example, you are applying for yourself, or a company you work for or own`

### Screen 04: Contact details

- If Screen 03 = `Yes`:
  - top H2: `Your contact details - as the agent, consultant or contractor`
  - intro line: `You must have authority to act on behalf of the licence holder to complete this form`
  - includes `Company name` after `Phone number`
- If Screen 03 = `No`:
  - top H2: `Licence holder details`
  - section heading: `Contact details`
  - section hint: `Contact details won’t appear on the licence`
- Static rows:
  - `Your name` / `[Login name]`
  - `Your email` / `[Login email]`
- Editable fields:
  - `Phone number`
  - `Company name` when Screen 03 = `Yes`
  - `Address line 1`
  - `Address line 2 (optional)`
  - `Town or city`
  - `Country (optional)`
  - `Post code`
- Language section:
  - `Preferred contact language`
  - hint: `Select the language we should use to contact you`
  - radios: `Welsh`, `English`
- Bottom actions:
  - `Back`
  - `Save and continue`
  - `Save and go to task list`

### Screens 05 to 14

These remain the working freshwater fish permit journey screens, with validation and back behaviour implemented in `work/freshwater-fish-flows-prototype/index.html`.

## Validation Rules

- Radio questions require one selected option before continuing.
- On the conditional contact-details screen, required fields are:
  - `Phone number`
  - `Company name` when Screen 03 = `Yes`
  - `Address line 1`
  - `Town or city`
  - `Post code`
  - `Preferred contact language`
- On the conditional contact-details screen, these are not editable user inputs:
  - `Your name`
  - `Your email`
- National Grid Reference is required.
- what3words is optional.
- Privacy and declaration checkboxes are required before continuing.

## Navigation Rules

- `Go back to task list` returns to the applications dashboard.
- `Save and go to task list` on the conditional contact-details screen also returns to the applications dashboard.
- Back behaviour on the new pre-task screens is:
  - Screen 03 back → applications dashboard or completed task-list review, depending on where the user came from
  - Screen 04 back → Screen 03
  - Screen 05 back → Screen 04 when shown, otherwise Screen 03

## Known Prototype Constraints

- `Marine licensing` and `Land access` are visible only and do not have working journeys.
- The old `Who is the licence for?` screen remains in the file but is not part of the live new-permit route.
- The review screen uses fixed example values rather than fully bound live answers.
- The current implementation is a prototype flow, not a production data model.
