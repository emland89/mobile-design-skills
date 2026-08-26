# watchOS behavioral conventions

Use current Apple HIG for watchOS as authority.

## Mental model
**Watch != tiny phone.** Apple Watch is worn, frequently glanced at, often used while moving, and optimized for brief, timely interactions. Start by deciding which moments deserve the wrist at all.

## Rules
- Prioritize wrist-appropriate value: often critical/timely information and one or a few targeted actions. Deeper standalone experiences are valid when sustained wrist use is intrinsic to the product; drop phone features that do not earn wrist time.
- Favor quick, glanceable, shallow interactions and minimize hierarchy depth.
- Treat complications, widgets/Smart Stack, notifications, Siri/shortcuts, and the app as parts of one experience; the full app need not be the primary entry point.
- Anchor vertical navigation and precise adjustment to the Digital Crown where appropriate, while providing corresponding touch interaction.
- Use Always On and wrist-raise context appropriately; do not require prolonged attention for routine tasks.
- Prefer vertical progression/pagination over deep or horizontally complex navigation when the platform guidance supports it.
- Keep essential actions usable in motion and avoid interaction that demands fine precision or long text entry.
- Design the watch app to provide useful independent value when the product permits it; use phone handoff/companion flows for tasks that genuinely belong on the larger device.
- Provide immediate, concise feedback and let asynchronous work finish without forcing the wrist to stay raised.
- Preserve accessibility, sufficient control sizing/spacing, readable text, and non-haptic/non-color alternatives.

## Scope test
Before adding a watch feature ask: Is it timely? Is it glanceable? Can it be completed quickly? Does wrist access improve it? Should this instead be a complication/widget/notification? Should the detailed task continue on phone?
