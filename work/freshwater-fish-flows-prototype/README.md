# Freshwater Fish Flows Prototype

Working prototype for the freshwater fish permit journey.

Main implementation file:

- `work/freshwater-fish-flows-prototype/index.html`

## Current Journey

The prototype currently includes:

1. Service landing screen
2. Applications dashboard
3. Check-your-answers review screen
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
- `Apply for a new permit` starts the new permit journey.
- `Continue`, `View`, and `Amend` from the dashboard all open the review screen.
- The `Licence holder details` screen is conditional and only appears for:
  - `An individual`
  - `No` to applying on behalf of someone else

## Build Rule

Do not invent screens, branches, question wording, options, evidence requirements, or review-page content.

If the built prototype changes, update the knowledge files in `outputs/` so they stay in sync.
