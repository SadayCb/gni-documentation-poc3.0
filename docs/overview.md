# Overview

`GAIA.LOAN_API` exposes Oracle PL/SQL operations spanning the loan lifecycle. This documentation is generated from the supplied specification and body, not from runtime inspection.

- **Loan operations and controls:** 6 public declarations; `get_trn_caller_id`, `add_months_for_loan`, `get_offer_id`, `is_online_offer`, `do_loan_control`, `do_loan_control`.
- **Accounts, guarantees and closure:** 8 public declarations; `get_account_feature`, `create_account`, `get_new_acc`, `do_loan_collateral_out`, `do_guarantee_out`, `do_Loan_Close_With_Collateral_Out`, `do_non_cash_loan_close`, `change_account_status`.
- **Payments and balances:** 5 public declarations; `get_amount_by_range`, `get_loan_amount`, `generate_allocated_payment_list`, `add_payment_details`, `do_Auto_Payment`.
- **Payment schedules and dates:** 24 public declarations; `post_int_amount_to_plan`, `get_overdue_grace_days`, `get_formatted_grace_from_list`, `get_grace_info`, `get_commission_schedule`, `get_next_Plan_Pym`, `get_plan_payment_amount`, `get_Plan_Month_Count`, …
- **Interest, penalties and rates:** 18 public declarations; `get_amount_for_pen_calc`, `get_interest_calc_info`, `get_interest_calc_dates`, `get_interest_calc_dates_ex`, `do_delete_operation`, `get_basis_year_days_cnt`, `loan_int_diff_operation`, `Get_Delay_Int_Rate`, …
- **Delinquency and status:** 6 public declarations; `get_ovd_trs_oper_type`, `get_overdue_min_amount`, `get_ovd_date`, `get_ovd_date_old`, `do_loan_status_control`, `get_acc_type_by_status`.
- **Limits, tranches and overdrafts:** 4 public declarations; `evaluate_limit_amount`, `do_create_tranche`, `create_overdrafts`, `get_new_ov_cont_no`.
- **Accounting and audit:** 9 public declarations; `add_column_update`, `add_column_update`, `get_voucher_data_from_query`, `get_gl_value`, `get_gl_acc_active_passive`, `get_gl_acc_from_matrix`, `do_journal_entry`, `create_journal_entries`, …
- **History, metadata and reversal:** 11 public declarations; `clear_addtional_data`, `add_additional_group`, `end_additional_group`, `add_additional_info`, `add_additional_info`, `get_additional_info`, `finalize_addtional_process`, `reverse_update`, …

[API reference](docs/api/loan-api.md)
