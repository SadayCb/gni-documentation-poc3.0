# Data model — observed SQL references

The following objects were extracted from direct SQL syntax in supplied public method segments. They may include aliases/CTEs or other non-table identifiers; object type and foreign keys were **not independently verified**.

| SQL object token | References | Method / operation |
|---|---:|---|
| `LOAN_PAYMENT_PLAN` | 26 | **READ**: [post_int_amount_to_plan](api/loan-api.md#post-int-amount-to-plan), [get_amount_for_pen_calc](api/loan-api.md#get-amount-for-pen-calc-1), [get_ovd_trs_oper_type](api/loan-api.md#get-ovd-trs-oper-type), [get_grace_info](api/loan-api.md#get-grace-info), [get_next_Plan_Pym](api/loan-api.md#get-next-plan-pym), [get_plan_payment_amount](api/loan-api.md#get-plan-payment-amount), [get_ovd_date](api/loan-api.md#get-ovd-date), [get_ovd_date_old](api/loan-api.md#get-ovd-date-old), [get_amount_for_pen_calc](api/loan-api.md#get-amount-for-pen-calc-2) (+9 others); **UPDATE**: [post_int_amount_to_plan](api/loan-api.md#post-int-amount-to-plan), [recalculate_int_payment_plan](api/loan-api.md#recalculate-int-payment-plan), [do_overdue_transit_operation](api/loan-api.md#do-overdue-transit-operation), [do_schedule_allignment](api/loan-api.md#do-schedule-allignment); **INSERT**: [table_log_operation](api/loan-api.md#table-log-operation), [do_overdue_transit_operation](api/loan-api.md#do-overdue-transit-operation), [UPDATE_PAYMENT_PLAN](api/loan-api.md#update-payment-plan); **DELETE**: [table_log_operation](api/loan-api.md#table-log-operation) |
| `KRD_TEKLIF_DETAY` | 21 | **READ**: [evaluate_limit_amount](api/loan-api.md#evaluate-limit-amount), [reverse_update](api/loan-api.md#reverse-update), [do_create_tranche](api/loan-api.md#do-create-tranche), [get_gl_acc_from_matrix](api/loan-api.md#get-gl-acc-from-matrix), [Get_Delay_Int_Rate](api/loan-api.md#get-delay-int-rate), [get_plan_payment_amount](api/loan-api.md#get-plan-payment-amount), [get_ovd_date](api/loan-api.md#get-ovd-date), [get_ovd_date_old](api/loan-api.md#get-ovd-date-old), [create_account](api/loan-api.md#create-account) (+8 others); **UPDATE**: [create_account](api/loan-api.md#create-account), [do_overdue_transit_operation](api/loan-api.md#do-overdue-transit-operation), [do_Loan_Close_With_Collateral_Out](api/loan-api.md#do-loan-close-with-collateral-out), [create_overdrafts](api/loan-api.md#create-overdrafts) |
| `CS_ACCOUNT` | 20 | **READ**: [evaluate_limit_amount](api/loan-api.md#evaluate-limit-amount), [get_loan_amount](api/loan-api.md#get-loan-amount), [get_gl_acc_from_matrix](api/loan-api.md#get-gl-acc-from-matrix), [get_ovd_date](api/loan-api.md#get-ovd-date), [get_ovd_date_old](api/loan-api.md#get-ovd-date-old), [get_account_feature](api/loan-api.md#get-account-feature), [get_new_acc](api/loan-api.md#get-new-acc), [update_loan_history](api/loan-api.md#update-loan-history), [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out) (+9 others); **UPDATE**: [do_Loan_Delay_Int_Rate_Upd](api/loan-api.md#do-loan-delay-int-rate-upd), [create_overdrafts](api/loan-api.md#create-overdrafts) |
| `LOAN_OPERATION_HISTORY` | 9 | **READ**: [get_additional_info](api/loan-api.md#get-additional-info), [reverse_update](api/loan-api.md#reverse-update), [do_delete_operation](api/loan-api.md#do-delete-operation), [do_loan_control](api/loan-api.md#do-loan-control-2), [create_loan_history](api/loan-api.md#create-loan-history), [update_loan_history](api/loan-api.md#update-loan-history); **INSERT**: [create_loan_history](api/loan-api.md#create-loan-history); **UPDATE**: [create_loan_history](api/loan-api.md#create-loan-history); **MERGE**: [update_loan_history](api/loan-api.md#update-loan-history) |
| `KRD_TESIS` | 8 | **READ**: [create_account](api/loan-api.md#create-account), [do_commission_recognition](api/loan-api.md#do-commission-recognition), [do_guarantee_out](api/loan-api.md#do-guarantee-out), [do_non_cash_loan_close](api/loan-api.md#do-non-cash-loan-close), [do_com_schedule_allignment](api/loan-api.md#do-com-schedule-allignment), [do_Loan_Delay_Int_Rate_Upd](api/loan-api.md#do-loan-delay-int-rate-upd), [init_global_variables](api/loan-api.md#init-global-variables); **UPDATE**: [create_account](api/loan-api.md#create-account) |
| `KRD_KOM_PLAN_DETAY` | 6 | **READ**: [table_log_operation](api/loan-api.md#table-log-operation), [do_commission_recognition](api/loan-api.md#do-commission-recognition), [do_com_schedule_allignment](api/loan-api.md#do-com-schedule-allignment); **INSERT**: [table_log_operation](api/loan-api.md#table-log-operation); **DELETE**: [table_log_operation](api/loan-api.md#table-log-operation); **UPDATE**: [do_com_schedule_allignment](api/loan-api.md#do-com-schedule-allignment) |
| `LOAN_FLOW_RATIO_INFO` | 5 | **READ**: [table_log_operation](api/loan-api.md#table-log-operation), [do_int_calculation](api/loan-api.md#do-int-calculation), [get_flow_ratio_info](api/loan-api.md#get-flow-ratio-info); **INSERT**: [table_log_operation](api/loan-api.md#table-log-operation); **DELETE**: [table_log_operation](api/loan-api.md#table-log-operation) |
| `LOAN_STOP_RATIO_INFO` | 5 | **READ**: [table_log_operation](api/loan-api.md#table-log-operation), [do_int_calculation](api/loan-api.md#do-int-calculation), [get_stop_ratio_info](api/loan-api.md#get-stop-ratio-info); **INSERT**: [table_log_operation](api/loan-api.md#table-log-operation); **DELETE**: [table_log_operation](api/loan-api.md#table-log-operation) |
| `IN_LIST` | 4 | **READ**: [get_loan_amount](api/loan-api.md#get-loan-amount), [create_account](api/loan-api.md#create-account), [generate_allocated_payment_list](api/loan-api.md#generate-allocated-payment-list), [do_Auto_Payment](api/loan-api.md#do-auto-payment) |
| `LOAN_ACC_TYPES_PR` | 4 | **READ**: [post_int_amount_to_plan](api/loan-api.md#post-int-amount-to-plan), [get_amount_for_pen_calc](api/loan-api.md#get-amount-for-pen-calc-1), [create_account](api/loan-api.md#create-account), [get_new_acc](api/loan-api.md#get-new-acc) |
| `LOAN_INT_CALCULATION_DIFF_HISTORY` | 4 | **READ**: [loan_int_diff_operation](api/loan-api.md#loan-int-diff-operation); **INSERT**: [loan_int_diff_operation](api/loan-api.md#loan-int-diff-operation); **UPDATE**: [loan_int_diff_operation](api/loan-api.md#loan-int-diff-operation); **DELETE**: [loan_int_diff_operation](api/loan-api.md#loan-int-diff-operation) |
| `LOAN_OPERATION_DESC` | 4 | **READ**: [get_trn_caller_id](api/loan-api.md#get-trn-caller-id), [create_journal_entries](api/loan-api.md#create-journal-entries), [create_loan_history](api/loan-api.md#create-loan-history), [update_loan_history](api/loan-api.md#update-loan-history) |
| `CARDS_ALL` | 3 | **READ**: [evaluate_limit_amount](api/loan-api.md#evaluate-limit-amount), [create_overdrafts](api/loan-api.md#create-overdrafts); **UPDATE**: [create_overdrafts](api/loan-api.md#create-overdrafts) |
| `ENTRIES_LIST_TAB` | 3 | **READ**: [do_journal_entry](api/loan-api.md#do-journal-entry); **INSERT**: [do_journal_entry](api/loan-api.md#do-journal-entry); **DELETE**: [do_journal_entry](api/loan-api.md#do-journal-entry) |
| `EOD_PROGRAMS_EXCEPTION` | 3 | **READ**: [do_Auto_Payment](api/loan-api.md#do-auto-payment), [do_int_calculation](api/loan-api.md#do-int-calculation), [create_overdrafts](api/loan-api.md#create-overdrafts) |
| `GLBL_TRANSACTION` | 3 | **READ**: [do_create_tranche](api/loan-api.md#do-create-tranche), [create_loan_history](api/loan-api.md#create-loan-history); **UPDATE**: [do_delete_operation](api/loan-api.md#do-delete-operation) |
| `GL_JOURNAL_LINES` | 3 | **READ**: [do_delete_operation](api/loan-api.md#do-delete-operation), [create_loan_history](api/loan-api.md#create-loan-history), [update_loan_history](api/loan-api.md#update-loan-history) |
| `KRD_KOM_EOD` | 3 | **READ**: [do_commission_recognition](api/loan-api.md#do-commission-recognition); **INSERT**: [do_commission_recognition](api/loan-api.md#do-commission-recognition); **UPDATE**: [do_commission_recognition](api/loan-api.md#do-commission-recognition) |
| `KRD_KOM_PLAN_DETAY_LOG` | 3 | **READ**: [table_log_operation](api/loan-api.md#table-log-operation); **INSERT**: [table_log_operation](api/loan-api.md#table-log-operation); **DELETE**: [table_log_operation](api/loan-api.md#table-log-operation) |
| `LOAN_CATEGORY` | 3 | **READ**: [table_log_operation](api/loan-api.md#table-log-operation); **INSERT**: [table_log_operation](api/loan-api.md#table-log-operation); **DELETE**: [table_log_operation](api/loan-api.md#table-log-operation) |
| `LOAN_CATEGORY_TEMP` | 3 | **READ**: [table_log_operation](api/loan-api.md#table-log-operation); **INSERT**: [table_log_operation](api/loan-api.md#table-log-operation); **DELETE**: [table_log_operation](api/loan-api.md#table-log-operation) |
| `OPERATIONS.` | 3 | **UPDATE**: [add_additional_info](api/loan-api.md#add-additional-info-1), [add_column_update](api/loan-api.md#add-column-update-1), [table_log_operation](api/loan-api.md#table-log-operation) |
| `GAIA.KRD_TEKLIF_DETAY` | 2 | **READ**: [UPDATE_PAYMENT_PLAN](api/loan-api.md#update-payment-plan); **UPDATE**: [UPDATE_PAYMENT_PLAN](api/loan-api.md#update-payment-plan) |
| `IBS.ONLINE_CRD_BLOCK` | 2 | **READ**: [UPDATE_PAYMENT_PLAN](api/loan-api.md#update-payment-plan); **UPDATE**: [UPDATE_PAYMENT_PLAN](api/loan-api.md#update-payment-plan) |
| `KRD_SCOR_AUTO_C` | 2 | **READ**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out); **UPDATE**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out) |
| `KRD_SCOR_EMANET_C` | 2 | **READ**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out); **UPDATE**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out) |
| `KRD_SCOR_ESYA_C` | 2 | **READ**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out); **UPDATE**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out) |
| `KRD_SCOR_QARANT_C` | 2 | **READ**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out); **UPDATE**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out) |
| `KRD_SCOR_REAL_ESTATE_C` | 2 | **READ**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out); **UPDATE**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out) |
| `KRD_SCOR_SEHMLER_C` | 2 | **READ**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out); **UPDATE**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out) |
| `KRD_SCOR_TEMINAT_ALAKA_C` | 2 | **READ**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out); **UPDATE**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out) |
| `KRD_SCOR_ZAMIN_C` | 2 | **READ**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out); **UPDATE**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out) |
| `KRD_SKOR_GIROV_OTHER_C` | 2 | **READ**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out); **UPDATE**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out) |
| `KRD_TEKLIF_NO` | 2 | **INSERT**: [get_offer_id](api/loan-api.md#get-offer-id); **UPDATE**: [get_offer_id](api/loan-api.md#get-offer-id) |
| `LOAN_EOD_AUTO_CLOSE` | 2 | **READ**: [do_Loan_Close_With_Collateral_Out](api/loan-api.md#do-loan-close-with-collateral-out); **INSERT**: [do_Loan_Close_With_Collateral_Out](api/loan-api.md#do-loan-close-with-collateral-out) |
| `LOAN_EOD_CONTROL` | 2 | **READ**: [do_loan_control](api/loan-api.md#do-loan-control-1); **INSERT**: [do_loan_control](api/loan-api.md#do-loan-control-2) |
| `LOAN_EOD_CONTROL_EXP` | 2 | **READ**: [do_plan_control](api/loan-api.md#do-plan-control), [do_loan_control](api/loan-api.md#do-loan-control-2) |
| `LOAN_FLOW_RATIO_INFO_LOG` | 2 | **READ**: [table_log_operation](api/loan-api.md#table-log-operation); **INSERT**: [table_log_operation](api/loan-api.md#table-log-operation) |
| `LOAN_INT_CALC_TYPES_PR` | 2 | **READ**: [get_interest_calc_info](api/loan-api.md#get-interest-calc-info), [get_basis_year_days_cnt](api/loan-api.md#get-basis-year-days-cnt) |
| `LOAN_PAYMENT_PLAN_LOG` | 2 | **READ**: [table_log_operation](api/loan-api.md#table-log-operation); **INSERT**: [table_log_operation](api/loan-api.md#table-log-operation) |
| `LOAN_PORTFOLIO_LITE` | 2 | **READ**: [do_loan_status_control](api/loan-api.md#do-loan-status-control), [do_Loan_Close_With_Collateral_Out](api/loan-api.md#do-loan-close-with-collateral-out) |
| `LOAN_STOP_RATIO_INFO_LOG` | 2 | **READ**: [table_log_operation](api/loan-api.md#table-log-operation); **INSERT**: [table_log_operation](api/loan-api.md#table-log-operation) |
| `LOAN_TEMPORARY_PAYMENT_PLAN` | 2 | **READ**: [UPDATE_PAYMENT_PLAN](api/loan-api.md#update-payment-plan); **INSERT**: [UPDATE_PAYMENT_PLAN](api/loan-api.md#update-payment-plan) |
| `LOAN_TRANCHE_PAYMENT_PLAN` | 2 | **READ**: [post_int_amount_to_plan](api/loan-api.md#post-int-amount-to-plan); **UPDATE**: [post_int_amount_to_plan](api/loan-api.md#post-int-amount-to-plan) |
| `ODEME_PLAN_TMP2` | 2 | **READ**: [get_special_schedule](api/loan-api.md#get-special-schedule); **UPDATE**: [get_special_schedule](api/loan-api.md#get-special-schedule) |
| `PKRD_TURKOD_PR` | 2 | **READ**: [get_overdue_min_amount](api/loan-api.md#get-overdue-min-amount), [get_overdue_grace_days](api/loan-api.md#get-overdue-grace-days) |
| `SS_MUH1201_0_LOG` | 2 | **READ**: [do_journal_entry](api/loan-api.md#do-journal-entry), [create_journal_entries](api/loan-api.md#create-journal-entries) |
| `ACTIONS.` | 1 | **UPDATE**: [create_loan_history](api/loan-api.md#create-loan-history) |
| `CREATE_SCHEDULE_PARAMETRS` | 1 | **READ**: [get_created_schedule](api/loan-api.md#get-created-schedule) |
| `GAIA.CS_ACCOUNT` | 1 | **READ**: [get_ovd_date](api/loan-api.md#get-ovd-date) |
| `GAIA.KRD_TESIS` | 1 | **UPDATE**: [UPDATE_PAYMENT_PLAN](api/loan-api.md#update-payment-plan) |
| `GAIA.LOAN_CATEGORY` | 1 | **READ**: [evaluate_limit_amount](api/loan-api.md#evaluate-limit-amount) |
| `GAIA.LOAN_OPERATION_HISTORY` | 1 | **READ**: [evaluate_limit_amount](api/loan-api.md#evaluate-limit-amount) |
| `GAIA.LOAN_PAYMENT_PLAN` | 1 | **READ**: [get_ovd_trs_oper_type](api/loan-api.md#get-ovd-trs-oper-type) |
| `GL_ACCOUNT_DEFINE` | 1 | **READ**: [get_gl_acc_active_passive](api/loan-api.md#get-gl-acc-active-passive) |
| `GL_URUN_HESAP_PR` | 1 | **READ**: [get_gl_acc_from_matrix](api/loan-api.md#get-gl-acc-from-matrix) |
| `KRD_FON_VERILME` | 1 | **UPDATE**: [do_Loan_Close_With_Collateral_Out](api/loan-api.md#do-loan-close-with-collateral-out) |
| `KRD_GUARANTEE_MAIN` | 1 | **READ**: [get_amount_for_pen_calc](api/loan-api.md#get-amount-for-pen-calc-1) |
| `KRD_ODEME_PLAN` | 1 | **READ**: [init_global_variables](api/loan-api.md#init-global-variables) |
| `KRD_SCOR_MAIN` | 1 | **READ**: [is_online_offer](api/loan-api.md#is-online-offer) |
| `KRD_SCOR_ODEME_PLAN` | 1 | **READ**: [get_schedule_from_memo](api/loan-api.md#get-schedule-from-memo) |
| `KRD_TEKLIF` | 1 | **READ**: [init_global_variables](api/loan-api.md#init-global-variables) |
| `KRD_TEMINAT_TIP_PR` | 1 | **READ**: [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out) |
| `LOAN` | 1 | **READ**: [get_acc_type_by_status](api/loan-api.md#get-acc-type-by-status) |
| `LOAN_ACCOUNTS` | 1 | **READ**: [create_account](api/loan-api.md#create-account) |
| `LOAN_ACC_TYPE_MAPPING` | 1 | **READ**: [get_acc_type_by_status](api/loan-api.md#get-acc-type-by-status) |
| `LOAN_AMOUNT_RANGE_INFO` | 1 | **READ**: [get_amount_by_range](api/loan-api.md#get-amount-by-range) |
| `LOAN_API.GET_GL_ACC_FROM_MATRIX` | 1 | **READ**: [create_account](api/loan-api.md#create-account) |
| `LOAN_GLOBAL_PARAMETERS_PR` | 1 | **READ**: [get_gl_value](api/loan-api.md#get-gl-value) |
| `LOAN_HISTORY_MAPPING` | 1 | **READ**: [add_column_update](api/loan-api.md#add-column-update-1) |
| `LOAN_INT_CALC_STOP_FOR_GRACE` | 1 | **READ**: [do_int_calculation](api/loan-api.md#do-int-calculation) |
| `LOAN_OPERATION_VOUCHER` | 1 | **READ**: [create_journal_entries](api/loan-api.md#create-journal-entries) |
| `LOAN_OVERDUE_MAPPING` | 1 | **READ**: [do_overdue_transit_operation](api/loan-api.md#do-overdue-transit-operation) |
| `LOAN_OVERDUE_TRANSIT_QUEUE` | 1 | **READ**: [do_overdue_transit_operation](api/loan-api.md#do-overdue-transit-operation) |
| `LOAN_SPECIAL_DAYS_PR` | 1 | **READ**: [get_amount_for_pen_calc](api/loan-api.md#get-amount-for-pen-calc-2) |
| `LOAN_TRANCHE_INFO` | 1 | **READ**: [add_column_update](api/loan-api.md#add-column-update-1) |
| `LOAN_TRANCHE_LIMIT_CHANGES_HISTORY` | 1 | **READ**: [do_Loan_Close_With_Collateral_Out](api/loan-api.md#do-loan-close-with-collateral-out) |
| `ODEME_PLAN_TMP` | 1 | **READ**: [UPDATE_PAYMENT_PLAN](api/loan-api.md#update-payment-plan) |
| `PAYMENT` | 1 | **UPDATE**: [UPDATE_PAYMENT_PLAN](api/loan-api.md#update-payment-plan) |
| `SP_FAIZ_GUN_TANIM_PR` | 1 | **READ**: [create_account](api/loan-api.md#create-account) |
| `SP_URUN_PR` | 1 | **READ**: [get_gl_acc_from_matrix](api/loan-api.md#get-gl-acc-from-matrix) |
| `TEMP_CARD_BALANCE` | 1 | **INSERT**: [create_overdrafts](api/loan-api.md#create-overdrafts) |

Do not interpret SQL joins as declared foreign keys without DDL.
