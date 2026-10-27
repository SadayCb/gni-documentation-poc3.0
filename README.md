# GAIA.LOAN_API — Technical Documentation

## 1. General

| Section | Item | Details / Reference |
|:--|:--|:--|
| **General** | Document Name | **LOAN_API — Technical & Functional Documentation** |
| | Package Name | `GAIA.LOAN_API` |
| | Created Date | 27 October 2026 |
| | Created By | GNI Software — Development Team |
| | Document Version | 1.0 — Draft |
| | Documentation Status | Under Technical & Business Review |
| | Technology | Oracle PL/SQL · Oracle Database |
| **Introduction** | Purpose of the Document | [Purpose & Overview](docs/overview.md) — Package objectives, responsibilities and scope. |
| | Scope of the Document | Public interfaces and verified implementation behavior. [Getting Started](docs/guides/getting-started.md) |
| | System Architecture | [Architecture](docs/architecture.md) — Components, dependencies and execution flow. |
| **API Specifications** | Procedures & Functions | [Complete API Reference](docs/api/loan-api.md) — Public procedures, functions and overloads. |
| | Business Workflows | [Business Workflows](docs/workflows.md) — Loan operations, schedules, payments and EOD/SOD processes. |
| | Technical Dependencies | [Dependencies](docs/reference/dependencies.md) — Related packages, procedures and functions. |
| **Data Model** | Tables & Views | [Data Model](docs/data-model.md) — Related database objects and data operations. |
| | Data Relationships | [Data Model & Relationships](docs/data-model.md) — Read/write interactions and dependencies. |
| **Error Handling** | Errors & Exceptions | [Error Handling Reference](docs/error-handling.md) — Application errors, validation rules and exception handling. |
| | Review Findings | [Technical Review Findings](docs/reference/review-findings.md) — Potential issues and unverified behavior. |

## 2. Introduction

**Purpose of the Document:** Developer onboarding, maintenance, banking-process knowledge transfer, and customer technical reference.

**Scope of the Document:** All 91 public procedure/function declarations identified in the supplied specification, with matching body evidence where available. Included: signatures, categorized API index, dependencies, execution evidence, error notes, and validation findings.

**Package Overview:** `LOAN_API` provides loan lifecycle services in an Oracle-based core banking environment. Its exposed methods span account and journal creation, payment plans, interest and penalties, delinquency transition, EOD/SOD processing, and limits/tranches.

**Main Responsibilities:** Loan account operations; calculation and payment schedules; automatic loan servicing; accounting and audit entries; loan history, metadata and status processing.

**Intended Audience:** PL/SQL developers, architects, support engineers, new employees, and customer technical teams.

## 3. API Specifications

**Public declarations:** 91; **distinct public names:** 87; **overloaded names:** 4.

### Functional Categories

- [Loan operations and controls](docs/api/loan-api.md#get-trn-caller-id) — 6 declarations
- [Accounts, guarantees and closure](docs/api/loan-api.md#get-account-feature) — 8 declarations
- [Payments and balances](docs/api/loan-api.md#get-amount-by-range) — 5 declarations
- [Payment schedules and dates](docs/api/loan-api.md#post-int-amount-to-plan) — 24 declarations
- [Interest, penalties and rates](docs/api/loan-api.md#get-amount-for-pen-calc-1) — 18 declarations
- [Delinquency and status](docs/api/loan-api.md#get-ovd-trs-oper-type) — 6 declarations
- [Limits, tranches and overdrafts](docs/api/loan-api.md#evaluate-limit-amount) — 4 declarations
- [Accounting and audit](docs/api/loan-api.md#add-column-update-1) — 9 declarations
- [History, metadata and reversal](docs/api/loan-api.md#clear-addtional-data) — 11 declarations

**Full reference:** [Complete public API](docs/api/loan-api.md)  
**Major dependencies:** [Dependency reference](docs/reference/dependencies.md)  
**Architecture:** [Architecture](docs/architecture.md)

## 4. Data Model

The data model includes loan offer/detail records, account and journal structures, payment plans, loan history, and product/rule configurations. Relationships shown are **code-level references**, not asserted database foreign keys.

See [Data model](docs/data-model.md).

## 5. Error Handling

Methods may use shared `R(...)` application reporting, explicit exception handlers, and validation conditions. Exact behavior of referenced external routines must be confirmed separately.

See [Error handling](docs/error-handling.md) and [Review findings](docs/reference/review-findings.md).

## Documentation Navigation

- [Start here](docs/index.md)
- [System overview](docs/overview.md)
- [Execution workflows](docs/workflows.md)
- [Developer guide](docs/guides/getting-started.md)
- [Static validation report](VALIDATION_REPORT.md)

> **Source limitation:** Database DDL, external package bodies, runtime configuration and live tests were not provided. Static references do not establish complete transitive dependencies or transactional behavior.
