# UX process

Use this when the product problem is greenfield, ambiguous, or large enough that screen-first work would create churn.

## Sequence
1. State the user and the job they are trying to accomplish.
2. Identify the moment that triggers use and the expected outcome.
3. Separate must-have tasks from infrequent/administrative tasks.
4. Model the happy path without screens.
5. Add decisions, interruptions, errors, permissions, and recovery.
6. Group information by user mental model, not backend/domain object shape alone.
7. Choose platform navigation patterns that fit the relationships.
8. Define screen responsibilities and state contracts.
9. Run accessibility/adaptation checks.
10. Prototype and test the riskiest assumptions first.

## Questions that expose weak UX
- What can the person do here, and which action matters most?
- What do they need to know before acting?
- What happens if they change their mind?
- What if the network, permission, device, or data is unavailable?
- What state survives leaving and returning?
- What must be discoverable without onboarding?
- Is complexity coming from the user's problem or our implementation?

## Evidence labels
When reviewing, label rationale mentally as one of:
- platform requirement/guidance
- accessibility requirement/guidance
- established usability principle
- product evidence
- design judgment/hypothesis

Do not present a preference as a platform rule.
