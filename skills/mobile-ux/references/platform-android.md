# Android behavioral conventions

Use current Android Developers and Material guidance as authority when current behavior matters.

## Principles
- Preserve Android navigation/back expectations.
- Choose navigation components based on destination structure and available window size.
- Adapt navigation on larger windows; Android guidance explicitly recommends alternatives such as navigation rail rather than retaining phone bottom navigation everywhere.
- Use canonical adaptive patterns (for example list-detail/supporting pane) where they improve the task.
- Treat 48x48 dp as the recommended minimum focusable touch area for touch interfaces.
- Support system accessibility semantics, font scaling, keyboard/pointer, and window resizing.
- Avoid iOS-specific interaction conventions copied for brand consistency when Android users would interpret them differently.
- Material components are conventions/tools, not a requirement that every branded product look identical.
