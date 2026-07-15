# Freshwater Fish Flows Prototype

Working prototype for the freshwater fish permit journey.

Main implementation file:

- `work/freshwater-fish-flows-prototype/index.html`

## Current Journey

The prototype currently includes:

1. Service landing screen
2. Applications dashboard
3. Shared application review screen
4. New permit journey starting with licence-holder questions
5. Freshwater fish application flow through declaration

## Source Of Truth

Use these files before changing the prototype:

- `outputs/freshwater-fish-flows-screen-plan.md`
- `outputs/codex-prototype-design-system.md`
- `outputs/design-agent-brief.md`
- `work/nrw-prototype-components/`

## Important Behaviour

- Only `Freshwater fish permits` is active on the landing screen.
- `Apply for a new permit` now starts at `Are you applying on behalf of someone else?`
- After that question, the journey shows a contact-details screen.
- If the user answers `Yes`, it shows the contractor version with `Company name`.
- If the user answers `No`, it shows the existing `Licence holder details` version.
- `View`, `Continue`, and `Amend` from the dashboard all open the same shared review screen.
- In the stocking route, `Tell us about your site` is followed by `Does your site have conservation designation?`
- The water step is now a combined screen with heading, subtitle, `name`, and `Type of water`.
- If `Canal` or `River` is selected, the water step reveals the fish-health message, a National Grid Reference field, and `Upstream limit` / `Downstream limit`.
- If `Stillwater` is selected, the water step reveals a single National Grid Reference field, size, `Is it landlocked or on-line?`, and `is it on a flood plain`.
- The old `Who is the licence for?` screen is no longer part of the live journey.
- The permit type labels are `Keep & introduce fish (a site permit)`, `Supplying fish (a fish supply permit)`, and `Removing fish`.

## Build Rule

Do not invent screens, branches, question wording, options, evidence requirements, or review-page content.

If the built prototype changes, update the knowledge files in `outputs/` so they stay in sync.
