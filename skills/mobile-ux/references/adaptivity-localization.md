# Adaptivity and localization

## Adaptivity
Design for available window and interaction context, not a fixed phone portrait screenshot.

- A larger window may change navigation and composition rather than scale elements up.
- Consider list-detail, supporting pane, denser comparison, and simultaneous context where useful.
- Keep readable content widths sensible instead of stretching text/forms edge to edge.
- Preserve task continuity across resize/orientation/multitasking.
- Consider pointer/keyboard/stylus input on devices that support them.
- Test compact, medium, and large/expanded contexts relevant to the platform.

## Localization
- Expect text expansion and contraction.
- Avoid fixed widths based on English labels.
- Keep icons culturally understandable; pair ambiguous icons with labels.
- Support RTL mirroring where semantics require it, while not mirroring directional media/symbols whose meaning should remain fixed.
- Do not encode meaning through word order that cannot survive localization.
- Avoid concatenated sentence fragments.
- Test dates, numbers, pluralization, names, and longer localized labels.

## Form-factor transformation
Do not equate responsiveness with proportional resizing.

- Phone: prioritize touch-first, interruption-tolerant, focused task completion; never begin by shrinking desktop chrome.
- Tablet/large window: consider simultaneous context, persistent navigation, and additional input modes, but add UI only when it improves the task.
- Foldable: respond to available window and posture without assuming a single permanent two-pane layout.
- Watch: reduce product scope to timely, glanceable, wrist-appropriate moments; do not preserve phone feature parity.
- Multi-platform: define invariants (goal, content model, terminology, brand semantics) separately from adaptations (navigation, controls, layout, modality, density, surfaces).
