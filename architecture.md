# Architecture

```mermaid
flowchart TD
    A[Calling banking modules and EOD SOD jobs] --> B[GAIA.LOAN_API public methods]
    B --> C[Loan account and payment plan processing]
    B --> D[Interest, delinquency and schedules]
    B --> E[Journal and history processing]
    C --> F[(Oracle loan and account tables)]
    D --> F
    E --> F
    B --> G[Referenced Oracle packages]
```

This is a **conceptual grouping of verified public capabilities**, not a complete runtime call graph. See [dependency index](reference/dependencies.md) and [API reference](api/loan-api.md) for directly observed references. Private routines are implementation details and may be invoked by public methods. No cross-package implementation was supplied.
