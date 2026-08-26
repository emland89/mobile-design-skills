# UX review checklist

## Purpose
- Can the primary user goal be stated in one sentence?
- Is the primary action obvious without onboarding?

## Flow
- Is the frequent path short without becoming cryptic?
- Can users cancel, back out, or recover without losing unexpected work?
- Are dependencies/permissions requested when relevant?

## IA/navigation
- Are top-level destinations truly peers?
- Are actions distinct from destinations?
- Is modal presentation used for bounded tasks rather than structural avoidance?

## State
- Empty/loading/offline/error/permission/success states are designed.
- Refresh and interrupted work preserve context when possible.

## Feedback/errors
- Every consequential action has immediate feedback.
- Errors explain what happened and what can be done next.
- Destructive actions have recovery or proportional confirmation.

## Accessibility
- No color/motion/sound/gesture-only meaning.
- Reading/focus order is meaningful.
- Large text and assistive input do not break the flow.
- Touch targets are adequate for the target platform.

## Adaptation
- Large windows are not just stretched phone layouts.
- Navigation/panes/density adapt when task value justifies it.
- Localization and RTL have been considered.

## Final test
If the interface were rendered in plain grayscale wireframes, would the task still be understandable and complete? If not, the UX is depending on visual polish to hide structural problems.
