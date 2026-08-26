# iPadOS behavioral conventions

Use current Apple HIG and iPadOS guidance as authority when current behavior matters.

## Mental model
An iPad experience is touch-first and mobile, but it can support longer sessions, multiple windows, multitasking, keyboard, pointer, Pencil, drag and drop, and simultaneous information. Do not treat it as either a stretched iPhone or a miniature Mac.

## Rules
- Design for the **current window**, not an assumed full-screen device size. The app may run beside other apps or in a resized window.
- Recompose when simultaneous context improves the task: sidebar/content, list-detail, inspectors/supporting regions, or other multi-column structures can reduce drill-down and backtracking.
- Do not add panes just to fill space. Preserve focus when one region is enough.
- Prefer iPad-native navigation and presentation choices where they improve efficiency; avoid modal-heavy phone flows on large windows when persistent context is better.
- Support touch first, then exploit keyboard, pointer/trackpad, Pencil, drag and drop, and focus where relevant to the product.
- Preserve standard keyboard shortcuts and platform focus behavior rather than inventing desktop conventions.
- Handle orientation, multitasking, resizing, and state preservation without losing the user's place.
- Keep readable content widths intentional; large windows do not justify edge-to-edge forms or text.
- Test compact iPad windows too: an iPad can temporarily need phone-like composition because the window is narrow.

## Transformation questions
From iPhone to iPad ask: What can become simultaneous? What navigation can become persistent? What repeated drilling can disappear? Which commands benefit from keyboard/pointer/Pencil? What should remain focused rather than becoming denser?
