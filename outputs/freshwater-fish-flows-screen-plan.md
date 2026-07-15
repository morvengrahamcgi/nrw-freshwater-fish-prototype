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
6. Stocking-only site and conservation questions
7. Combined water-details screen, then location, environment, fish, privacy, and declaration screens
8. `Check your answers before submitting your application`

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
- `View`, `Continue`, and `Amend` all open the completed application review screen.
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
| 02 | Check your answers before submitting your application | Built | Opens from `View`, `Continue`, and `Amend`. Uses NRW summary cards for `Licence holder details`, `Permit`, `Fish`, `Privacy notice`, and `Declaration`. Bottom actions are `Back` and `Complete`. |
| 03 | Are you applying on behalf of someone else? | Built | Radio question with `Yes` and `No`, both with hint text. This is now the first screen in the new-permit journey. |
| 04 | Contact details | Built | Shared contact-details step shown after Screen 03. If the user answers `Yes`, this becomes `Your contact details - as the agent, consultant or contractor` and includes `Company name` after `Phone number`. If the user answers `No`, it uses the existing `Licence holder details` version. |
| 05 | Which task are you planning on completing? | Built | Radio question with `Keep & introduce fish (a site permit)`, `Supplying fish (a fish supply permit)`, `Removing fish`. Back returns to Screen 04 when the contact-details branch is present, otherwise Screen 03. |
| 06 | Tell us about your site | Built | Stocking-only screen shown immediately after `Keep & introduce fish (a site permit)` is selected. Includes `What is the name of the site?` and a `Site address` section with address fields. |
| 07 | Does your site have conservation designation? | Built | Stocking-only radio question with `Yes`, `No`, `Unknown`. If `Yes` is selected, a checkbox reveal shows `Site of Special Scientific Interest (SSSI)`, `Special Area of Conservation (SAC)`, and `Ramsar sites`. |
| 08 | Water details | Built | Combined water-entry screen. H2 is `Please provide details about the relevant bodies of water on your site for this permit`, subtitle is `Add your water bodies in one at a time`, then a `name` text field and `Type of water` radios. `Canal` and `River` reveal the fish-health message, a National Grid Reference heading with helper text, and free-text `Upstream limit` / `Downstream limit` fields. `Stillwater` reveals a single National Grid Reference field, `What is the size of the water?`, `Is the water landlocked or on line?`, and `is it on a flood plain`. |
| 09 | What is the nearest town/city of your proposed activity? | Built | Text input question with the supporting line `This will appear on your application form`. |
| 10 | Provide a National Grid Reference / Provide a what3words (optional) | Built | Two-question page. National Grid Reference is required. what3words is optional. |
| 11 | Are any of the fish a non-native species? | Built | Radio question with `Yes`, `No`, `Unknown`. |
| 12 | Are there any crayfish present? | Built | Radio question with `Yes`, `No`, `Unknown`. |
| 13 | Fish | Built | Progressive add-to-list page. Starts with one fish-entry state, then moves to an added-fish summary state with `Change`, `Remove`, and `Do you need to add another type of fish?` |
| 14 | How we use your personal data | Built | Checkbox confirmation page with `I have read and understood this information`. |
| 15 | Declaration | Built | Checkbox confirmation page with `To the best of my knowledge and belief, the information I have given is correct`. |

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

### Screen 06: Tell us about your site

- Shown only when Screen 05 = `Keep & introduce fish (a site permit)`
- Top H2:
  - `Tell us about your site`
- First question:
  - `What is the name of the site?`
  - supporting text: `This will be used to help identify your application. If you’re registered with CEFAS, please use the same name. If you’re not registered, please provide a new name`
  - input placeholder: `Site name`
- Second section:
  - `Site address`
- Address fields:
  - `Address line 1`
  - `Address line 2 (optional)`
  - `Town or city`
  - `County (optional)`
  - `Post code`
- Bottom actions:
  - `Back`
  - `Save and continue`
  - `Save and go to task list`

### Screen 07: Does your site have conservation designation?

- Shown only in the stocking route, immediately after Screen 06
- Main question:
  - `Does your site have conservation designation?`
- Radio options:
  - `Yes`
  - `No`
  - `Unknown`
- If `Yes` is selected, reveal these checkboxes:
  - `Site of Special Scientific Interest (SSSI)`
  - `Special Area of Conservation (SAC)`
  - `Ramsar sites`
- Bottom actions:
  - `Back`
  - `Save and continue`
  - `Save and go to task list`

### Screen 08: Water details

- Used for both stocking and non-stocking routes
- Main heading:
  - `Please provide details about the relevant bodies of water on your site for this permit`
- Subtitle:
  - `Add your water bodies in one at a time`
- Fields shown on the same screen:
  - `name`
  - `Type of water`
- Radio options:
  - `Canal`
  - `River`
  - `Stillwater`
- If `Canal` or `River` is selected, reveal:
  - `Fish health check required. Because this water is connected to other water bodies, you'll need to obtain a fish health check certificate from your fish supplier`
  - `Provide a National Grid Reference for your water’s location`
  - support text linking to `UK Grid Reference Finder`
  - `Upstream limit`
  - `Downstream limit`
- If `Stillwater` is selected, reveal:
  - `Provide a National Grid Reference for your water’s location`
  - support text linking to `UK Grid Reference Finder`
  - `What is the size of the water?`
  - `Is the water landlocked or on line?`
  - `Landlocked`
  - hint: `No connections to other bodies of water`
  - `On-line`
  - hint: `Has connecting inlets/outlets, ie, a stream`
  - `is it on a flood plain`
  - support text linking to `Flood Risk Assessment Wales Map`

### Screens 05 to 15

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
- On the stocking-only site screen, required fields are:
  - `Site name`
  - `Address line 1`
  - `Town or city`
  - `Post code`
- On the conservation-designation screen, the radio question is required.
- On the water-details screen, required inputs are:
  - `name`
  - `Type of water`
- If `Canal` or `River` is selected, `Provide a National Grid Reference for your water’s location` is required.
- If `Stillwater` is selected, these are required:
  - `Provide a National Grid Reference for your water’s location`
  - `What is the size of the water?`
  - `Is the water landlocked or on line?`
  - `is it on a flood plain`
- On the conditional contact-details screen, these are not editable user inputs:
  - `Your name`
  - `Your email`
- National Grid Reference is required.
- what3words is optional.
- Privacy and declaration checkboxes are required before continuing.

## Navigation Rules

- `Go back to task list` returns to `Check your answers before submitting your application`.
- `Save and go to task list` on the conditional contact-details screen also returns to `Check your answers before submitting your application`.
- Back behaviour on the new pre-task screens is:
  - Screen 03 back → applications dashboard or completed task-list review, depending on where the user came from
  - Screen 04 back → Screen 03
  - Screen 05 back → Screen 04 when shown, otherwise Screen 03
  - Screen 06 back → Screen 05
  - Screen 07 back → Screen 06
  - Screen 08 back → Screen 07 in the stocking route, otherwise Screen 05

## Known Prototype Constraints

- `Marine licensing` and `Land access` are visible only and do not have working journeys.
- The review screen uses fixed example values rather than fully bound live answers.
- The current implementation is a prototype flow, not a production data model.
