# Wear OS behavioral conventions

Use current Android Developers Wear OS guidance as authority.

## Mental model
**Watch != tiny phone.** Optimize first for critical tasks that can be completed quickly, with shallow structure and wrist-appropriate entry surfaces. Allow deeper standalone experiences when the product genuinely benefits from sustained watch use.

## Rules
- Keep app tasks focused, shallow, and usually linear; avoid deep hierarchies.
- Optimize for vertical layouts and scrolling.
- Support rotary input for essential scrolling/selection where hardware provides it, with visible response and touch alternatives.
- Treat Tiles, complications, notifications, voice actions, and the app as complementary surfaces. A glanceable surface may be a better home than a full app screen.
- Keep Tiles glanceable and action-focused; do not reproduce detailed phone dashboards on the wrist.
- Account for round/compact displays and edge reachability rather than designing a rectangular phone canvas and clipping it.
- Reduce scope instead of shrinking controls or packing more rows onto small displays.
- Use the phone/companion experience for complex creation, configuration, or long-form input when appropriate.
- Preserve accessibility, adequate touch targets, readable type, and alternatives to color/haptic-only meaning.

## Scope test
Ask whether the watch makes the task faster, more contextual, or more glanceable. If not, omit it. Cross-platform product parity does not require feature parity on the watch.
