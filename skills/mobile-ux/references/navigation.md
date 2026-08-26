# Navigation

Navigation communicates the product's structure. Choose it from destination relationships and frequency.

## General rules
- Keep top-level navigation stable and predictable.
- Distinguish navigation (go somewhere) from actions (do something here).
- Preserve expected back behavior and state restoration.
- Avoid deep modal stacks.
- Use modality for focused, bounded tasks or decisions, not as an escape hatch from IA.
- Preserve current selection/context on larger list-detail layouts.
- Do not hide frequent destinations behind overflow merely to make the chrome cleaner.

## Review questions
- Can users predict where a destination will be?
- Does back mean the same kind of thing throughout the flow?
- Are top-level destinations truly peers?
- Is a modal dismissible without losing unexpected work?
- Would this model still make sense with large text, keyboard input, or a larger window?
