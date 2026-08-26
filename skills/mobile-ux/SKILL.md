---
name: mobile-ux
description: Design or critique how native mobile and wearable experiences work across iOS, iPadOS, Android phones/tablets/foldables, watchOS, and Wear OS. Use when deciding user flows, information architecture, navigation, interaction models, gestures, forms, states, feedback, recovery, accessibility, ergonomics, adaptivity, localization, companion/watch scope, or platform-native behavior. Use before visual styling when behavior or structure is unresolved. Do not use as the primary skill for visual art direction or implementation code.
license: MIT
compatibility: "Portable Agent Skills format; requires file/reference reading. Web access is optional and used only to verify volatile platform guidance when available."
metadata:
  version: "1.3.0"
  synthesis: "OpenAI research synthesis, 2026-08-22"
---

# Mobile UX

Design the behavior of a mobile product so people can understand it, act confidently, recover from mistakes, and feel at home on the target platform.

## Boundary

Own **how the experience works**. Do not make visual-art-direction decisions unless they are necessary to communicate hierarchy or interaction.

UX owns:
- user goals, jobs, and task flows
- information architecture and navigation
- interaction models, gestures, disclosure, and modality
- input and form behavior
- empty/loading/error/offline/success states
- feedback, undo, confirmation, and recovery
- accessibility requirements and alternative interaction paths
- ergonomics, reachability, touch target intent, and input modality
- platform behavioral conventions
- adaptation across window sizes, orientation, devices, and localization

UX does not own:
- palette, decorative shape language, imagery style, visual texture, or brand art direction
- implementation framework or API selection
- ornamental animation

When UI and UX conflict, use this precedence unless product safety/domain requirements demand stricter treatment:
1. safety, data integrity, privacy, and irreversible harm prevention
2. accessibility and essential task completion
3. user comprehension, agency, and recovery
4. target-platform behavioral conventions
5. product-specific UX consistency
6. visual distinctiveness
7. cross-platform parity
8. implementation convenience

Platform conventions are strong defaults, not dogma. Deviate when product evidence or a domain requirement produces a clearly better outcome and the resulting behavior remains discoverable, accessible, and internally coherent.

## Form-factor invariants

Treat these as non-negotiable review heuristics, not slogans:
- **MOBILE != MINI DESKTOP.** Start from mobile context, touch, interruption, posture, and focused tasks rather than shrinking a desktop IA.
- **TABLET != LARGE PHONE.** Recompose navigation, panes, density, and input support when extra space improves the task.
- **WATCH != TINY PHONE.** A watch is a selective product surface, not a feature-parity target. First decide which capabilities genuinely earn wrist presence; omit the rest. Favor timely, glanceable, focused, sensor/context-aware or quick-action interactions, while allowing deeper standalone watch experiences only when sustained wrist use is intrinsic to the product.
- **ADAPT != SCALE.** Form factor can change structure, navigation, modality, information density, and available capabilities.
- **MORE SPACE != MORE UI.** Add simultaneous context only when it reduces navigation, comparison cost, or task friction.
- **SMALLER SPACE != CRAMMED UI.** Reduce scope and prioritize rather than compressing controls and content.
- **SAME PRODUCT != SAME INTERFACE.** Preserve goals, concepts, content, data, and identity while letting platform conventions reshape the experience.
- **CROSS-PLATFORM != PIXEL PARITY.** Never copy one platform wholesale merely to match screenshots.
- **CONSISTENCY != UNIFORMITY.** Be conceptually consistent and platform-native at the same time.
- **NATIVE != GENERIC; CUSTOM != BETTER.** Use familiar platform behavior while spending novelty only where it improves the product.

## Core principles

1. **Purpose before screens.** Start from the user's goal and the product's primary job, not from a dashboard or navigation shell.
2. **Familiar behavior, intentional product structure.** Reuse platform patterns where they match the mental model; invent only when the benefit is concrete and teachable.
3. **Recognition over memory.** Keep important choices, state, and consequences visible at the point of action.
4. **Agency and recovery.** Prefer reversible actions, clear exits, undo, drafts, and preservation of user work.
5. **Feedback closes every loop.** Every meaningful action needs perceivable acknowledgement, progress, success, failure, or changed state.
6. **Simplicity is not deletion.** Remove unnecessary complexity without hiding essential choices or context.
7. **Accessibility is architecture.** Do not bolt it on after the flow is designed.
8. **Adapt behavior, not just dimensions.** Larger or different windows may deserve different navigation, pane structure, and information density.
9. **Design all states, not only the happy path.** A flow is incomplete until interruptions, errors, permissions, latency, offline behavior, empty data, and recovery are considered.
10. **Evidence over preference.** Distinguish platform guidance, established usability principles, product evidence, and design judgment.
11. **Keep volatile platform facts fresh.** Stable human factors belong here; when current platform behavior, components, or guidelines matter and current official documentation is available through the agent’s tools/context, verify against it rather than treating this skill as frozen authority.

## Operating loop

### 1. Establish context

Determine, from available product material or repository context:
- target users and their primary goal
- platform(s): iOS, iPadOS, Android, watchOS, Wear OS, or a combination
- device/window scope: phone, tablet, foldable, watch, resizable/desktop-class windowing, etc.
- relationship among surfaces: standalone, companion, handoff, notification/widget/tile/complication entry points
- current product conventions or design system
- primary and secondary tasks
- constraints: safety, privacy, offline, permissions, latency, localization, accessibility

Do not block on missing noncritical information. State assumptions and proceed.

**Watch capability gate:** if watchOS or Wear OS is in scope, do not assume phone feature parity. Before designing watch screens, classify candidate capabilities:
- **Keep on watch** when wrist access materially improves timeliness, glanceability, immediate action, sensor/context use, haptics, workout/navigation/media-control continuity, or independent wearable value.
- **Use a watch surface instead of a full app flow** when a complication, widget/Smart Stack, Tile, notification, or quick action is sufficient.
- **Hand off / companion** when the task requires substantial creation, configuration, comparison, reading, precision, or text entry better suited to a larger device.
- **Omit** when the watch adds no meaningful advantage. "The phone has this feature" is never sufficient justification.

For watch targets, read the relevant watch platform reference before committing the feature set.

Read `references/process.md` when the problem is ambiguous or greenfield.

### 2. Model the task before the screen

Write the shortest successful path as user intent -> decision -> action -> feedback -> next state.

Identify:
- entry points
- primary path
- optional branches
- destructive or irreversible moments
- interruptions and resumption
- completion and post-completion destination

For complex flows, read `references/flows-ia.md`.

### 3. Choose the information and navigation model

Choose structure based on relationships among destinations and tasks, not visual preference.

Ask:
- What is global vs contextual?
- What must remain reachable from anywhere?
- Is this hierarchy, peer switching, drill-down, search, or a transient task?
- Does a modal actually protect focus, or merely avoid designing navigation?
- What should persist when a person returns?

Read `references/navigation.md` and the target platform reference.

### 4. Define interaction contracts

For every important control or gesture, specify:
- affordance / discoverability
- action
- immediate feedback
- state change
- cancellation / reversal
- accessibility equivalent
- failure behavior

Do not make a gesture the only route to essential functionality unless the platform convention and accessibility story support it.

Read `references/interaction-ergonomics.md`.

### 5. Design the complete state model

At minimum consider:
- first use / onboarding only if needed
- empty
- loading / progressive loading
- partially loaded
- populated
- refreshing
- offline / degraded
- validation error
- system / network error
- permission denied / restricted
- destructive confirmation where warranted
- success
- interrupted / resumable

Read `references/states-feedback.md` and `references/forms-input.md` as relevant.

### 6. Accessibility and inclusion gate

Check before visual polish:
- meaningful reading/focus order
- nonvisual labels and state announcements
- Dynamic Type / scalable text implications
- touch target and spacing intent
- no color-, motion-, sound-, or gesture-only meaning
- reduced-motion path
- keyboard/switch/pointer access where platform/device supports it
- plain, inclusive language
- time limits or auto-dismiss behavior

Read `references/accessibility.md`.

### 7. Form-factor transformation gate

Do not start from a reference screen and resize it. Start from the invariant user goal, then decide what this form factor should expose.

For each target, explicitly ask:
- What remains invariant across platforms/form factors?
- What changes because of platform convention?
- What changes because of posture, display, input, interruption, or window size?
- What should disappear rather than be squeezed in?
- What becomes more prominent or more glanceable?
- What can become simultaneous on a larger window?
- What belongs on a companion device or a system surface instead?
- For a watch: which proposed capabilities should be omitted entirely because wrist access adds no value?
- Can a user of this platform predict navigation, back/dismissal, input, and feedback?

Do not simply stretch the phone UI.

Consider:
- window size rather than device label alone
- multi-column/list-detail/supporting-pane opportunities
- navigation transformation on larger windows
- content width and readable line length
- portrait/landscape and multitasking
- fold posture or external input where relevant
- watch glanceability, brief interaction, rotary/hardware input, and companion/system surfaces where relevant
- localization expansion and RTL

Read `references/adaptivity-localization.md` and the specific platform/form-factor reference.

### 8. Calibrate when the problem is easy to misread

Read `references/calibration-examples.md` when the request involves cross-platform parity, desktop-to-mobile conversion, phone-to-tablet transformation, or phone-to-watch feature selection. Use the examples to calibrate decisions, not as templates to copy.

### 9. Self-critique before delivery

Run `references/review-checklist.md`.

Perform at least two internal passes:
- **Friction pass:** remove unnecessary steps, recall, mode switches, hidden dependencies, and dead ends.
- **Failure pass:** attempt to break the flow with cancellation, back navigation, double action, timeout, offline state, permission denial, large text, and interrupted progress.

Revise before presenting the result.

## Gotchas

- Do not infer that every product needs a watch app merely because watchOS/Wear OS is listed as a supported platform.
- Do not interpret "native" as "copy first-party apps"; preserve platform mental models while allowing product-specific structure.
- Do not use device labels as fixed breakpoints when window size, posture, or input mode provides better evidence.
- Do not turn an audit request into a full redesign when a smaller correction solves the problem.
- Do not load every platform reference. Read only the references for targets actually in scope.

## Platform routing

Read only what applies:
- iPhone/iOS: `references/platform-ios.md`
- iPad/iPadOS: `references/platform-ipados.md` (and iOS when shared Apple behavior matters)
- Android phones: `references/platform-android.md`
- Android tablets/foldables/large windows: `references/platform-android-large-screen.md` (and Android base guidance)
- Apple Watch/watchOS: `references/platform-watchos.md`
- Wear OS watches: `references/platform-wearos.md`
- cross-platform or multi-form-factor: read every targeted reference; preserve shared product semantics while allowing platform-native behavior and form-factor-specific scope

Never use pixel parity as a UX requirement. If a product brief asks for identical navigation or interaction across platforms, challenge that constraint when it conflicts with established platform expectations.

## Collaboration contract with mobile-ui

Provide UI with:
- screen purpose and priority
- information hierarchy
- interaction/state contracts
- navigation model
- accessibility requirements
- motion intent (what must be communicated, not how it looks)
- haptic intent (meaning, not decorative pattern)

UI may propose changes when visual communication exposes a hierarchy problem. Re-evaluate the UX rather than defending the first solution.

## Output

For greenfield or redesign work, return:
1. goals and assumptions
2. primary task flow
3. information/navigation model
4. screen/region responsibilities
5. interaction contracts
6. state matrix
7. accessibility requirements
8. adaptation rules
9. open risks/tradeoffs
10. platform/form-factor transformation matrix when more than one target is in scope
11. UX handoff to UI

For audits, prioritize findings by user harm and frequency, then explain the principle and the smallest effective change.

## Non-goals and anti-patterns

Reject:
- starting with a generic dashboard, cards, or tabs before understanding the task
- copying another platform's navigation merely for visual consistency
- hiding core actions behind gestures or overflow without reason
- modal stacks that trap the user
- destructive actions without proportional recovery/confirmation
- spinners with no context for long or uncertain waits
- forms that erase entered data after errors
- onboarding that teaches obvious platform conventions
- forcing account creation or permissions before their value is clear unless genuinely required
- phone layouts stretched onto tablets or large windows
- desktop information architecture shrunk onto phones
- phone feature trees copied onto watches
- pixel-identical cross-platform behavior that violates native expectations
- adding controls merely because a larger display has room
- accessibility treated as a final checklist only
