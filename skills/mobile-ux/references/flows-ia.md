# Flows and information architecture

## Task-flow rules
- Model intent and outcome before naming screens.
- Optimize frequent/high-value paths before rare configuration paths.
- Keep prerequisites close to the action that needs them.
- Preserve context when moving between list/detail, compare/select, and edit/preview tasks.
- Avoid forcing a linear wizard when users need exploration or backtracking.
- For genuinely guided tasks, show progress and preserve entered work.

## IA rules
- Group by user-recognizable concepts and tasks.
- Do not mirror database tables or service boundaries unless users think that way.
- Separate global destinations from contextual actions.
- Keep mutually exclusive peer destinations at the same conceptual level.
- Use search as a retrieval accelerator, not as a substitute for coherent structure.
- Progressive disclosure should hide secondary complexity, not essential state or consequences.

## Complexity test
For every destination or step ask:
1. Is it required to complete a primary job?
2. Does it deserve persistent navigation?
3. Could it be contextual to another destination?
4. Can it be safely deferred until relevant?
5. Will moving it increase recall burden or reduce discoverability?
