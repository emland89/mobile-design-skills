---
name: mobile-ui
description: Create or critique the visual expression of native mobile and wearable interfaces across iOS, iPadOS, Android phones/tablets/foldables, watchOS, and Wear OS. Use when the UX model is known and the task concerns visual direction, hierarchy, composition, typography, color, spacing, shape, surfaces/materials, iconography, imagery, motion expression, haptic presentation, design systems, cross-platform visual expression, or anti-generic/anti-template review. Do not use to invent navigation/behavior or implementation code.
license: MIT
compatibility: "Portable Agent Skills format; requires file/reference reading. Web access is optional and used only to verify volatile platform guidance when available."
metadata:
  version: "1.3.0"
  synthesis: "OpenAI research synthesis, 2026-08-22"
---

# Mobile UI

Give a mobile product a clear visual point of view without making it stop feeling native, usable, or accessible.

## Boundary

Own **how the experience looks and feels**, given a sound UX model.

UI owns:
- visual concept and product-specific design direction
- visual hierarchy and composition
- typography, color, spacing, rhythm, shape, surfaces, and depth
- iconography and imagery direction
- component appearance and state differentiation
- motion expression and transition choreography
- visual/haptic polish
- design tokens and visual-system consistency
- platform visual conventions
- anti-generic / anti-template review

UI does not own:
- changing navigation, behavior, destructive semantics, or information architecture solely for aesthetics
- implementation framework/API choice
- hiding required accessibility information to make the screen cleaner

When visual novelty conflicts with comprehension, accessibility, or platform behavior, redesign the visual treatment instead of breaking the interaction.

When constraints conflict, use the same precedence as mobile-ux: safety/data integrity/privacy -> accessibility/task completion -> comprehension/agency/recovery -> platform conventions -> product UX consistency -> visual identity -> cross-platform parity -> implementation convenience. Platform visual conventions are strong defaults, not a requirement to imitate first-party apps; deviate deliberately when identity or domain needs justify it without harming recognizability or usability.

## Cross-platform invariants

- **SAME PRODUCT != SAME INTERFACE.** Preserve recognizable product identity without forcing the same components or composition everywhere.
- **CROSS-PLATFORM != PIXEL PARITY.** Pixel identity is not a quality target. Native fluency outranks screenshot matching.
- **CONSISTENCY != UNIFORMITY.** Share semantic design decisions; let each platform express them through its own visual grammar.
- **TABLET != ENLARGED PHONE.** Recompose hierarchy and density instead of scaling phone artboards.
- **WATCH != SHRUNK PHONE.** Visual design follows the watch feature set selected by UX; never make omitted phone features reappear merely to achieve visual or feature parity. Design retained watch capabilities for glanceability, focus, compact geometry, and platform-native surfaces.
- **ADAPT != SCALE.** Typography, composition, density, materials, controls, and motion may all transform with context.
- **NATIVE != GENERIC.** A platform-native app can still have a strong, product-specific visual identity.

## Core principles

1. **Ground aesthetics in the product.** Derive the visual language from the subject, audience, content, environment, and emotional goal—not from fashionable UI tropes.
2. **Native does not mean generic.** Platform conventions establish fluency; product identity supplies character.
3. **Intentionality beats intensity.** A restrained interface can be distinctive. Boldness is not the same as gradients, glass, shadows, or animation everywhere.
4. **One memorable idea is stronger than many decorative ideas.** Spend visual risk deliberately, then keep supporting elements disciplined.
5. **Hierarchy before decoration.** Scale, position, type, contrast, grouping, and whitespace should communicate structure before effects are added.
6. **Content is the material.** Let real content shape composition; do not wrap everything in interchangeable cards.
7. **Depth must communicate relationships.** Materials, blur, shadow, layering, and elevation are structural cues, not default embellishment.
8. **Motion explains change.** Choreography should preserve spatial/causal continuity, confirm state, or direct attention. Decorative motion is optional and subordinate.
9. **System components are raw material, not a visual prison.** Prefer platform-native semantics and behavior while customizing presentation where the platform permits and the product benefits.
10. **Craft is iterative.** Critique, remove, compare, and refine before accepting the first plausible design.
11. **Keep volatile platform visuals fresh.** Stable visual principles belong here; verify current official platform guidance, when available through the agent’s tools/context, before relying on current components, materials, visual language, or system capabilities.

## Operating loop

### 1. Consume UX before styling

Identify:
- screen purpose and primary action
- content hierarchy
- interaction and navigation contracts
- states and errors
- accessibility constraints
- platform(s) and form factors
- which visual identity traits are invariant versus allowed to transform by platform/form factor

If those are absent, infer a minimal UX model or invoke/use the UX skill first. Do not invent a visual solution that conceals structural uncertainty.

### 2. Ground the visual direction

Before choosing colors or surfaces, define:
- product subject/world
- audience
- emotional target (for example calm, precise, playful, editorial, energetic, trustworthy)
- 2-4 visual attributes
- one signature idea that could make this product recognizable
- what must remain quiet so the signature can work

Read `references/visual-direction.md`.

Avoid generic mood labels with no design consequence. Translate direction into specific choices in typography, composition, color, material, imagery, and motion.

### 3. Build hierarchy and composition

Establish the reading order with:
- scale
- alignment
- grouping
- whitespace
- contrast
- density
- repetition and interruption

Prefer structural variety when content warrants it; do not turn every region into the same rounded rectangle.

Read `references/hierarchy-composition.md`.

### 4. Define typography and color systems

Typography:
- choose semantic roles, hierarchy, weight/width/design variation, and numeric behavior deliberately
- support scalable text and avoid fragile fixed-size layouts
- use custom typography only when it earns its cost and remains accessible/platform-appropriate

Color:
- define roles, not a pile of hex values
- use a dominant neutral/content environment plus intentional accents when appropriate
- verify light/dark/high-contrast behavior
- never rely on color alone for meaning

Read `references/typography.md` and `references/color.md`.

### 5. Define spacing, shape, surfaces, and depth

Create a small coherent spacing rhythm, but allow optical correction and content-driven exceptions.

Use shape to express relationship, brand, or interaction state. Repeating identical radii on every container is not a system; it is a habit.

Use surfaces/materials to establish layering and context. Do not add glass, blur, shadow, or elevation without a reason.

Read `references/spacing-shape.md` and `references/surfaces-depth.md`.

### 6. Choose iconography and imagery intentionally

Prefer platform-standard symbols for conventional actions when they are clear. Custom icons/illustration should add identity or domain meaning, not merely replace familiar symbols.

Images should carry content, atmosphere, or recognition. Avoid meaningless stock-like decoration.

Read `references/iconography-imagery.md`.

### 7. Express motion and haptics

Start from UX intent: what relationship/change needs to be perceived?

Then choose the least motion that makes it clear and satisfying.

Prioritize:
- spatial continuity for navigation or object movement
- direct manipulation response
- state change emphasis
- entrance/exit only when it supports orientation
- reduced-motion alternatives
- haptics as reinforcement, never the sole signal

Read `references/motion-haptics.md`.

### 8. Platform and form-factor visual gate

Read only what applies:
- iPhone/iOS: `references/platform-ios.md`
- iPad/iPadOS: `references/platform-ipados.md`
- Android phones: `references/platform-android.md`
- Android tablets/foldables/large windows: `references/platform-android-large-screen.md`
- Apple Watch/watchOS: `references/platform-watchos.md`
- Wear OS watches: `references/platform-wearos.md`
- cross-platform: read every targeted reference; preserve brand/product identity through semantic roles, content voice, assets, and signature ideas while allowing components, density, composition, materials, and motion to be platform-native

If asked for pixel-identical platforms, reject pixel parity as the default goal. Define an **identity contract** (what must remain recognizable) and a **platform expression contract** (what should adapt).

### 9. Calibrate when platform expression is easy to over-unify

Read `references/calibration-examples.md` for cross-platform identity, phone-to-tablet recomposition, watch visual reduction, and anti-template examples. Use them as decision calibrators, never as layouts to copy.

### 10. Anti-generic critique

Run `references/anti-patterns.md` and `references/review-checklist.md`.

Perform at least three internal passes:
- **Template pass:** could this screen belong to an unrelated app after replacing the logo and text?
- **Restraint pass:** remove one decorative treatment at a time. If meaning and identity improve, keep it removed.
- **Platform pass:** would an experienced user recognize controls, hierarchy, and states without being taught the interface?
- **Parity pass (multi-platform only):** identify any element kept identical solely for screenshot parity; either justify it as product identity or adapt it to the platform.

Revise before presenting the design.

## Gotchas

- Do not restore features that UX intentionally removed from watch/tablet/mobile scope merely to make platforms look symmetrical.
- Do not interpret a shared design system as identical component geometry across platforms. Share semantics first; adapt expression.
- Do not make every screen visually distinctive. Spend novelty where it reinforces product identity or hierarchy; let supporting screens stay quiet.
- Do not treat anti-patterns as bans. A card, gradient, glass material, or dashboard is valid when the product structure and platform context justify it.
- Do not load every platform reference. Read only the references for targets actually in scope.

## Collaboration contract with mobile-ux

Do not silently rewrite UX. If visual work reveals:
- too many equal-priority actions
- ambiguous grouping
- impossible hierarchy
- unclear state distinctions
- navigation that cannot be represented cleanly

flag the issue and propose a UX change with rationale.

UI may own **how** motion looks; UX owns **why** it occurs and what state relationship it communicates.

## Output

For a new visual direction or redesign, return:
1. visual thesis
2. product-specific signature idea
3. hierarchy/composition rules
4. typography system
5. color roles
6. spacing/shape/surface rules
7. component/state visual behavior
8. imagery/iconography direction
9. motion/haptic expression
10. platform/form-factor identity + expression matrix when more than one target is in scope
11. anti-generic critique and what was deliberately removed
12. UI handoff constraints for implementation

For audits, identify the highest-impact visual problems first and distinguish system-level problems from local polish.

## Anti-patterns

Reject by default unless the product context specifically justifies them:
- dashboard-first composition for products that are not dashboards
- large title + subtitle + grid of interchangeable cards as a universal template
- every section in a rounded rectangle
- one corner radius applied to everything
- purple/blue gradient as default "premium/AI" identity
- glass/blur used everywhere because the platform supports it
- excessive shadows/elevation that flatten hierarchy by making everything elevated
- icon-only actions whose meaning is not obvious
- random SF Symbols/Material icons used as decoration
- weak type hierarchy with nearly identical sizes/weights
- centered layouts for content that benefits from stronger reading structure
- motion on every interaction
- excessive accent colors competing for attention
- fake depth that does not correspond to interaction or layer relationships
- visual novelty that forces custom navigation or hides standard controls
- pixel-identical iOS/Android/watch designs maintained at the expense of native visual grammar
- phone compositions merely enlarged for tablets
- phone compositions merely miniaturized for watches
