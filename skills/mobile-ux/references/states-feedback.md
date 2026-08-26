# States, feedback, and recovery

## State matrix
For every data-bearing screen, decide behavior for:
- first/empty
- loading
- partial content
- loaded
- refresh
- stale/offline
- recoverable error
- unrecoverable/restricted state
- permission required/denied
- success/confirmation

## Feedback rules
- Acknowledge taps/actions immediately even when work continues asynchronously.
- For uncertain waits, explain what is happening when useful; avoid indefinite context-free spinners.
- Preserve usable content during refresh when possible.
- Put validation near the source of error and retain entered data.
- Make success confirmation proportional to uncertainty and consequence.
- Prefer undo for easily reversible destructive actions; use confirmation when consequences are costly, surprising, or irreversible.
- Never make haptics, color, or transient toast-like UI the only evidence that an important action succeeded or failed.
