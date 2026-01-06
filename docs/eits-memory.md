# E-ITS Agent Memory

This file tracks decisions, patterns, and lessons learned regarding E-ITS compliance.

## Security Decisions

### [Example] Security Class Determination
**Context**: User data processing
**Decision**: Classified as K2T2S2 due to presence of personal identification codes (isikukood).

## Common Pitfalls

### Audit Logging
**Mistake**: Logging sensitive data in clear text.
**Correction**: Hash or mask sensitive fields (e.g. `pic=***`).
