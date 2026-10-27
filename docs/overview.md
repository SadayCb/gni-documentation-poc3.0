# LOAN_API — Package Overview

## 1. Purpose

`GAIA.LOAN_API` is a shared Oracle PL/SQL service package that provides reusable business and technical functionality for loan processing across the banking system.

The supplied package specification and body cover loan account operations, balances, payment allocation, repayment schedules, interest and penalty calculations, overdue handling, credit limits and tranches, accounting journal entries, operation history, and automated processing associated with EOD/SOD.

The package should be treated as **shared business infrastructure**, not as the controller of a single application screen. Its public procedures, functions, and types form an interface used by other banking components.

For method signatures and source-derived behavior, see the [Complete API Reference](api/loan-api.md).

## 2. Functional Areas

The public API is organized into the **same nine functional categories** used in the [API Reference](api/loan-api.md). Counts represent public declarations, including overloads as separate declarations.

| Functional Area | Public Declarations | Description |
|:--|--:|:--|
| **Loan operations and controls** | 6 | Loan-operation support functions, caller identification, offer-related utilities, and loan control processing. |
| **Accounts, guarantees and closure** | 8 | Loan account creation and features, account status changes, guarantee or collateral release, and loan closure operations. |
| **Payments and balances** | 5 | Loan amount retrieval, payment allocation and detail assembly, and automated loan payment processing. |
| **Payment schedules and dates** | 24 | Standard and annuity schedule generation, repayment dates, grace-period information, scheduled amounts, schedule checks, and adjustments. |
| **Interest, penalties and rates** | 18 | Interest-calculation periods and bases, interest processing, penalty calculation, rate information, and related financial calculations or operations. |
| **Delinquency and status** | 6 | Overdue date and threshold evaluation, delinquency transition decisions, and loan/account status handling. |
| **Limits, tranches and overdrafts** | 4 | Credit limit evaluation, tranche creation, and overdraft-related operations. |
| **Accounting and audit** | 9 | General-ledger mapping, journal entry generation and checking, voucher information, and change/audit support. |
| **History, metadata and reversal** | 11 | Additional operation information, grouped metadata, operation history, and reversal of tracked changes. |
| **Total** | **91** | **Public declarations, including overloaded variants.** |

These categories are **documentation navigation groups**, not isolated business modules. A method may participate in multiple processes even though it is documented under one primary category. For the complete method list, follow the [Public API Index](api/loan-api.md#public-api-index).

## 3. Technical Context

| Component | Description |
|:--|:--|
| **Package** | `GAIA.LOAN_API` |
| **Database Technology** | Oracle Database |
| **Programming Language** | Oracle PL/SQL |
| **Public Contract** | `LOAN_API` package specification: public procedures, functions, parameters, constants/state, and PL/SQL types. |
| **Implementation** | `LOAN_API` package body: business conditions, SQL statements, dependent calls, and exception handling. |
| **Public Data Types** | PL/SQL records and collections for loan accounts, journal entries, voucher fields, supplemental information, and date lists. |
| **Related Data** | Loan master/detail data, customer/account data, payment plans, transactions, accounting records, and histories, as evidenced by the supplied code. |
| **Integration** | Calls to other Oracle packages and database objects; some routines use Oracle database utilities. |
| **Operational Context** | Interactive loan transactions, scheduled processing, and EOD/SOD banking operations. |
| **Verification Scope** | Static examination of the supplied specification and body. Runtime results and implementations of external dependencies have not been independently verified. |

### Operational Considerations

Some public routines create or update accounts, modify payment plans, post accounting entries, process payments, or change loan-related records. Side effects and transaction behavior vary by method and should be reviewed in its individual API reference section.

**Safety note:** Do not execute data-changing or financially sensitive examples against production without an approved test plan, appropriate authorization, and verified input identifiers.

## 4. Related Documentation

- [Complete API Reference](api/loan-api.md) — public signatures, parameters, business logic, dependencies, and method-level notes.
- [System Architecture](architecture.md) — package relationships and major component interactions.
- [Business Workflows](workflows.md) — processing sequences and financial workflows.
- [Data Model](data-model.md) — relevant database objects and operations.
- [Error Handling](error-handling.md) — identifiable validation and exception behavior.
- [Technical Dependencies](reference/dependencies.md) — dependent packages and database objects.
- [Review Findings](reference/review-findings.md) — issues or assumptions requiring further review.
- [Getting Started](guides/getting-started.md) — orientation for developers new to the package.
