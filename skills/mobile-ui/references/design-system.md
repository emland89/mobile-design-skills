# Visual system handoff

Capture decisions as reusable roles, not arbitrary per-screen values.

## Minimum useful system
- typography roles
- semantic color roles
- spacing rhythm
- shape/radius roles if shape is part of identity
- surface/material roles
- iconography rules
- key component visual states
- motion principles/timing families
- light/dark/high-contrast behavior

## Avoid token theater
Do not create a token for every literal value just to appear systematic. A useful token represents a repeated semantic decision.

## Component state coverage
For interactive components consider:
- default
- pressed/active
- selected
- focused (where relevant)
- disabled
- loading
- destructive/warning
- error/validation

The visual system must not redefine UX semantics. If two states behave differently, that semantic distinction should come from UX/product requirements first.
