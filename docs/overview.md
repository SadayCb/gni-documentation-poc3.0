# LOAN_API — Package Overview

## 1. Purpose

`GAIA.LOAN_API` is a centralized Oracle PL/SQL service package that provides reusable business logic and technical functionality for loan management operations within the banking system.

The package supports core banking processes, including loan account management, financial calculations, payment schedule generation, payment processing, interest and penalty calculations, accounting journal entries, transaction history, and automated EOD/SOD operations.

It serves as **shared business infrastructure** used by multiple banking modules and processes, rather than being associated with a single application screen or operation.

For detailed specifications of individual procedures and functions, refer to the [API Reference](api/loan-api.md).

## 2. Functional Areas

The package contains public procedures and functions organized into the following functional areas:

| Functional Area | Description |
|:--|:--|
| **Accounts & Balances** | Loan account creation, account status management, balance retrieval, credit limit evaluation, and related account operations. |
| **EOD/SOD & Operations** | Automated daily banking operations, including loan controls, interest calculation, overdue processing, and automatic payments. |
| **History & Changes** | Loan transaction history, additional operation information, data modification tracking, and reversal operations. |
| **Interest & Penalties** | Interest calculation rules, overdue interest, penalty calculation bases, grace periods, and calculation date management. |
| **Journal & Vouchers** | Accounting journal generation, debit/credit transactions, general ledger account mapping, and voucher-related operations. |
| **Payments & Allocation** | Payment allocation, scheduled payment retrieval, payment distribution, and payment-related information processing. |
| **Schedules & Rates** | Standard and annuity payment schedules, commission schedules, repayment dates, grace periods, and variable interest rate information. |
| **Utilities & Configuration** | Supporting configuration and utility operations used by loan processing routines. |

The complete list of public procedures and functions is available in the [API Reference](api/loan-api.md).

## 3. Technical Context

| Component | Description |
|:--|:--|
| **Database Technology** | Oracle Database |
| **Programming Language** | Oracle PL/SQL |
| **Package Name** | `GAIA.LOAN_API` |
| **Public Interface** | `LOAN_API` Package Specification |
| **Implementation** | `LOAN_API` Package Body |
| **Custom Data Types** | PL/SQL records and collections for loan accounts, accounting entries, additional information, and date lists. |
| **Database Dependencies** | Loan, customer, account, payment schedule, transaction history, and accounting-related database objects. |
| **External Dependencies** | Other Oracle PL/SQL packages, system configuration components, and database utilities. |
| **Execution Context** | Banking transactions, loan operations, scheduled processes, and EOD/SOD execution. |

### Operational Considerations

Some procedures perform financial operations, modify loan-related records, generate accounting entries, or update transaction history.

**Important:** Procedures that modify financial or operational data must be tested in an authorized development or testing environment before production execution.

For further technical details, refer to:

- [System Architecture](architecture.md)
- [Business Workflows](workflows.md)
- [Data Model](data-model.md)
- [Technical Dependencies](reference/dependencies.md)
