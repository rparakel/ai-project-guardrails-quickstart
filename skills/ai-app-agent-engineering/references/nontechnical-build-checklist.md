# Non-Technical Build Checklist

Read this before you publish a showcase built with Base44, Dify, Lovable, Google AI Studio, Replit, or another prompt-driven builder.

Mark each item `PASS`, `FAIL`, or `NOT NEEDED`. A blank item is not a pass.

## Product

- [ ] You can name one primary user and the one task the project completes.
- [ ] The first screen makes the required input and next action clear.
- [ ] One complete workflow works from input to useful result.
- [ ] Extra features do not block or distract from that workflow.
- [ ] Sample content is clearly labeled as sample or synthetic.

## Inputs and AI behavior

- [ ] Required fields are validated before the AI runs.
- [ ] Missing information produces a clear request or `Unknown`, not an invented answer.
- [ ] The output separates supplied facts from AI interpretation.
- [ ] The normal, weak, and incomplete test cases produce acceptable results.
- [ ] Long or unexpected input does not break the page or return a false success.
- [ ] The agent has a retry limit and a visible error state.

## Data and access

- [ ] You know what data is stored, where it is stored, and who can see it.
- [ ] One user cannot access another user's records through the interface or a guessed URL.
- [ ] You are not using a real pitch deck, founder record, LP record, private email, or financial document.
- [ ] API keys and tokens are in the builder's secret store, not the prompt, frontend, repository, or screenshot.
- [ ] External connectors use the smallest available permissions.
- [ ] Sending, publishing, deleting, purchasing, inviting, and external updates require your confirmation.

## Interface

- [ ] Loading, empty, error, success, disabled, and permission-limited states are understandable.
- [ ] Every field has a visible label and every error explains how to recover.
- [ ] Keyboard focus is visible and the primary workflow works without a mouse where the builder supports it.
- [ ] Text and controls remain usable on a narrow phone and an ordinary laptop.
- [ ] Text contrast is readable and status is not communicated by color alone.

## Cost and dependencies

- [ ] You checked the current free-plan limits on the provider's official page.
- [ ] No billing account, paid model, paid deployment, or external API was enabled without your approval.
- [ ] You know which actions consume build credits and which consume runtime AI or integration credits.
- [ ] The project still demonstrates its main value if a paid or mocked integration is unavailable.

## Test and share

- [ ] You ran the relevant cases in the repository's `EVALS.md`.
- [ ] Every claim such as `fixed`, `passed`, or `deployed` has visible evidence.
- [ ] The shared link opens in a private browser window or on a device that is not signed into the builder.
- [ ] The published version matches the version you tested.
- [ ] The final page or documentation names mocked behavior, unverified checks, and production limitations.

## Handoff

Before you finish, save a short record of the goal, workflow, data fields, agent instructions, output schema, test results, free-plan dependencies, and remaining risks. This is enough for a teammate to understand the demonstration without reading the builder conversation.

