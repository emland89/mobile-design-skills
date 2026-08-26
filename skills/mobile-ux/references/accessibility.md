# Accessibility architecture

Accessibility changes structure, not just labels.

## Required design checks
- Reading/focus order matches meaning, not merely visual coordinates.
- Controls have meaningful accessible names, roles, values, and state changes.
- Important status changes can be perceived without sight/hearing/haptics.
- Text can scale without clipping, overlap, inaccessible truncation, or loss of actions.
- Color is never the sole carrier of status.
- Motion has a reduced-motion strategy.
- Time-limited/transient content does not block people who need more time.
- Touch targets and spacing support limited dexterity.
- Keyboard, switch, pointer, and assistive-navigation paths are considered where relevant.
- Custom controls do not lose standard semantics.

## Platform baselines
- Apple recommends familiar interactions, adaptable interfaces, and sufficiently sized controls; its accessibility guidance lists 44x44 pt as the default iOS/iPadOS control size and 28x28 pt as the stated minimum, while spacing also matters.
- Android recommends at least a 48x48 dp focusable/touch target for touch interfaces.
- WCAG is useful for cross-platform principles such as contrast, target size, and non-color-only communication, but do not mechanically substitute web-specific criteria for native platform guidance.
