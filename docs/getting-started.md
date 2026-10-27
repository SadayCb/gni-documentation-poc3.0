# Getting started

1. Read [the overview](../overview.md) and [the architecture](../architecture.md).
2. Use the [public API index](../api/loan-api.md) to locate the exact signature, including overloads.
3. Review the method's direct database effects, conditions, error excerpts, and referenced routines.
4. Validate parameter semantics and code values against product configuration and external package documentation.
5. Run tests only in a suitable non-production environment with approved sample identifiers.

**Transaction policy:** Do not assume a method is read-only because its name starts with `get`; inspect both direct and delegated effects. The caller must assess explicit and indirect transaction control.
