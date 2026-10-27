# External and qualified call references

Static occurrence-based reference inventory. Names may refer to SQL functions, package members or qualified schema objects, and do not confirm dependency validity or execution.

| Qualified reference | Public methods containing the reference |
|---|---|
| `APEX_JSON.GET_COUNT` | [get_created_schedule](../api/loan-api.md#get-created-schedule) |
| `APEX_JSON.GET_DATE` | [get_created_schedule](../api/loan-api.md#get-created-schedule) |
| `APEX_JSON.GET_NUMBER` | [get_created_schedule](../api/loan-api.md#get-created-schedule) |
| `APEX_JSON.OPEN_OBJECT` | [add_additional_group](../api/loan-api.md#add-additional-group) |
| `APEX_JSON.PARSE` | [get_created_schedule](../api/loan-api.md#get-created-schedule) |
| `APEX_JSON.WRITE` | [add_additional_info](../api/loan-api.md#add-additional-info-1) |
| `APEX_KRD2204_0_API_P.DEL_KRD2204_0` | [do_create_tranche](../api/loan-api.md#do-create-tranche) |
| `APEX_KRD2204_0_API_P.INS_KRD2204_0` | [do_create_tranche](../api/loan-api.md#do-create-tranche), [do_Auto_Payment](../api/loan-api.md#do-auto-payment) |
| `APEX_KRD2204_2_API_P.INS_KRD2204_2` | [do_Auto_Payment](../api/loan-api.md#do-auto-payment) |
| `APEX_KRD2204_7_API_P.INS_KRD2204_7` | [do_Auto_Payment](../api/loan-api.md#do-auto-payment) |
| `APEX_KRD2220_0_API_P.INS_KRD2220_0` | [do_guarantee_out](../api/loan-api.md#do-guarantee-out), [do_non_cash_loan_close](../api/loan-api.md#do-non-cash-loan-close) |
| `API_CALENDAR.GET_WORK_DAY` | [UPDATE_PAYMENT_PLAN](../api/loan-api.md#update-payment-plan) |
| `API_VISTA.P2P_TRANS_VALUE` | [create_overdrafts](../api/loan-api.md#create-overdrafts) |
| `BLOKE_API.BLOKE_KOY_KALDIR` | [do_loan_collateral_out](../api/loan-api.md#do-loan-collateral-out) |
| `CL.ACC_TYPE` | [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation) |
| `CL.LOAN_DOC_NO` | [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation) |
| `CR.ACC_TYPE` | [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation) |
| `CR.LOAN_DOC_NO` | [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation) |
| `DBMS_SQL.CLOSE_CURSOR` | [get_voucher_data_from_query](../api/loan-api.md#get-voucher-data-from-query) |
| `DBMS_SQL.COLUMN_VALUE` | [get_voucher_data_from_query](../api/loan-api.md#get-voucher-data-from-query) |
| `DBMS_SQL.DEFINE_COLUMN` | [get_voucher_data_from_query](../api/loan-api.md#get-voucher-data-from-query) |
| `DBMS_SQL.DESCRIBE_COLUMNS` | [get_voucher_data_from_query](../api/loan-api.md#get-voucher-data-from-query) |
| `DBMS_SQL.EXECUTE` | [get_voucher_data_from_query](../api/loan-api.md#get-voucher-data-from-query) |
| `DBMS_SQL.FETCH_ROWS` | [get_voucher_data_from_query](../api/loan-api.md#get-voucher-data-from-query) |
| `DBMS_SQL.IS_OPEN` | [get_voucher_data_from_query](../api/loan-api.md#get-voucher-data-from-query) |
| `DBMS_SQL.PARSE` | [get_voucher_data_from_query](../api/loan-api.md#get-voucher-data-from-query) |
| `GAIA.R` | [UPDATE_PAYMENT_PLAN](../api/loan-api.md#update-payment-plan) |
| `GLBL.SETUN` | [do_loan_control](../api/loan-api.md#do-loan-control-2) |
| `GLBL.TO_NUMBER#` | [loan_int_diff_operation](../api/loan-api.md#loan-int-diff-operation), [get_plan_error](../api/loan-api.md#get-plan-error) |
| `GLBL_BAKIYE.ACCOUNT_BALANCE` | [do_commission_recognition](../api/loan-api.md#do-commission-recognition) |
| `GLBL_BAKIYE.REAL_BALANCE` | [do_Auto_Payment](../api/loan-api.md#do-auto-payment), [do_guarantee_out](../api/loan-api.md#do-guarantee-out), [do_non_cash_loan_close](../api/loan-api.md#do-non-cash-loan-close) |
| `GLBL_CCY.GET_CUR_RATE` | [do_loan_collateral_out](../api/loan-api.md#do-loan-collateral-out), [do_Auto_Payment](../api/loan-api.md#do-auto-payment) |
| `GLBL_CCY.TO_CCY_MB` | [do_loan_collateral_out](../api/loan-api.md#do-loan-collateral-out) |
| `GLBL_EOD.GETCALLERID` | [do_loan_collateral_out](../api/loan-api.md#do-loan-collateral-out), [do_Loan_Close_With_Collateral_Out](../api/loan-api.md#do-loan-close-with-collateral-out) |
| `GLBL_FAIZ.DAYS_BETWEEN2` | [get_commission_schedule](../api/loan-api.md#get-commission-schedule), [get_Plan_Month_Count](../api/loan-api.md#get-plan-month-count), [get_Pym_Startdate](../api/loan-api.md#get-pym-startdate) |
| `GLBL_FAIZ.DAY_COUNT_BASIS_NEW` | [get_amount_for_pen_calc](../api/loan-api.md#get-amount-for-pen-calc-2), [recalculate_int_payment_plan](../api/loan-api.md#recalculate-int-payment-plan), [do_int_calculation](../api/loan-api.md#do-int-calculation), [get_schedule_from_memo](../api/loan-api.md#get-schedule-from-memo), [get_special_schedule](../api/loan-api.md#get-special-schedule) |
| `GLBL_FUNCTIONS.GUN_KUR_BUL` | [do_journal_entry](../api/loan-api.md#do-journal-entry) |
| `GLBL_HESAP.GET_ACCOUNT_PR` | [evaluate_limit_amount](../api/loan-api.md#evaluate-limit-amount), [get_gl_acc_from_matrix](../api/loan-api.md#get-gl-acc-from-matrix), [do_Loan_Close_With_Collateral_Out](../api/loan-api.md#do-loan-close-with-collateral-out) |
| `GLBL_HESAP.GET_ACC_CUR` | [do_journal_entry](../api/loan-api.md#do-journal-entry) |
| `GLBL_HESAP.HESAPNO_AC` | [change_account_status](../api/loan-api.md#change-account-status), [create_overdrafts](../api/loan-api.md#create-overdrafts) |
| `GLBL_HESAP.HESAPNO_KAPA` | [change_account_status](../api/loan-api.md#change-account-status), [create_overdrafts](../api/loan-api.md#create-overdrafts) |
| `GLBL_HESAP.YENI_M2_HESAPNO` | [get_new_acc](../api/loan-api.md#get-new-acc) |
| `GLBL_NAME.GET_CUSTOMER_NOVU_CODE` | [create_account](../api/loan-api.md#create-account) |
| `GLBL_TARIH.AYBASI` | [get_interest_calc_dates](../api/loan-api.md#get-interest-calc-dates), [get_interest_calc_dates_ex](../api/loan-api.md#get-interest-calc-dates-ex) |
| `GLBL_TARIH.AYSONU` | [do_commission_recognition](../api/loan-api.md#do-commission-recognition) |
| `GLBL_TARIH.DAYSBETWEEN` | [create_account](../api/loan-api.md#create-account) |
| `GLBL_TARIH.ONCEKI_ISGUNU` | [get_commission_schedule](../api/loan-api.md#get-commission-schedule), [get_Pym_Startdate](../api/loan-api.md#get-pym-startdate), [is_Payment_Date](../api/loan-api.md#is-payment-date), [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `GLBL_TARIH.SONRAKI_ISGUNU` | [get_interest_calc_dates](../api/loan-api.md#get-interest-calc-dates), [get_interest_calc_dates_ex](../api/loan-api.md#get-interest-calc-dates-ex), [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `GLOG.ASSERT#` | [do_com_schedule_allignment](../api/loan-api.md#do-com-schedule-allignment) |
| `GNI_MESSAGE.GET_MESSAGE` | [get_commission_schedule](../api/loan-api.md#get-commission-schedule), [get_Pym_Startdate](../api/loan-api.md#get-pym-startdate), [create_account](../api/loan-api.md#create-account), [get_new_acc](../api/loan-api.md#get-new-acc), [do_loan_status_control](../api/loan-api.md#do-loan-status-control) |
| `GNI_UTILITY.DELETE_BATCH_ERROR` | [do_Auto_Payment](../api/loan-api.md#do-auto-payment), [do_int_calculation](../api/loan-api.md#do-int-calculation), [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation) |
| `GNI_UTILITY.HAS_BATCH_ERROR` | [do_Auto_Payment](../api/loan-api.md#do-auto-payment), [do_int_calculation](../api/loan-api.md#do-int-calculation), [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation) |
| `GNI_UTILITY.LOG_BATCH_ERROR` | [do_Auto_Payment](../api/loan-api.md#do-auto-payment), [do_int_calculation](../api/loan-api.md#do-int-calculation), [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation) |
| `GNI_UTILITY.RUN_TASK` | [do_loan_control](../api/loan-api.md#do-loan-control-1) |
| `JSON_OBJECT_T.PARSE` | [get_additional_info](../api/loan-api.md#get-additional-info), [reverse_update](../api/loan-api.md#reverse-update) |
| `KRD2204_0_API.JUSTDOIT` | [do_create_tranche](../api/loan-api.md#do-create-tranche), [do_Auto_Payment](../api/loan-api.md#do-auto-payment) |
| `KRD2204_0_API.UPDATE_PAYMENT_PLAN` | [do_create_tranche](../api/loan-api.md#do-create-tranche), [do_Auto_Payment](../api/loan-api.md#do-auto-payment) |
| `KRD2220_0_API.JUSTDOIT` | [do_guarantee_out](../api/loan-api.md#do-guarantee-out), [do_non_cash_loan_close](../api/loan-api.md#do-non-cash-loan-close) |
| `KRD_EOD.GET_GL_URUN_HESAP` | [do_commission_recognition](../api/loan-api.md#do-commission-recognition) |
| `KRD_EOD.M_FIS_KES` | [do_commission_recognition](../api/loan-api.md#do-commission-recognition) |
| `KRD_EOD.TERS_FIS_KES` | [do_delete_operation](../api/loan-api.md#do-delete-operation) |
| `LA.ACC_TYPE` | [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.ADD_ADDITIONAL_INFO` | [evaluate_limit_amount](../api/loan-api.md#evaluate-limit-amount), [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.ADD_ADDITIONAL_MAIN_GROUP` | [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.ADD_COLUMN_UPDATE` | [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.ADD_INFO_TAB` | [create_overdrafts](../api/loan-api.md#create-overdrafts) |
| `LOAN_API.ADD_MONTHS_FOR_LOAN` | [get_Plan_Month_Count](../api/loan-api.md#get-plan-month-count), [UPDATE_PAYMENT_PLAN](../api/loan-api.md#update-payment-plan) |
| `LOAN_API.CHANGE_ACCOUNT_STATUS` | [do_Loan_Close_With_Collateral_Out](../api/loan-api.md#do-loan-close-with-collateral-out) |
| `LOAN_API.CLEAR_ADDTIONAL_DATA` | [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.CREATE_ACCOUNT` | [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation) |
| `LOAN_API.CREATE_LOAN_HISTORY` | [evaluate_limit_amount](../api/loan-api.md#evaluate-limit-amount), [do_delete_operation](../api/loan-api.md#do-delete-operation), [do_int_calculation](../api/loan-api.md#do-int-calculation), [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation), [do_Loan_Close_With_Collateral_Out](../api/loan-api.md#do-loan-close-with-collateral-out), [UPDATE_PAYMENT_PLAN](../api/loan-api.md#update-payment-plan) |
| `LOAN_API.CREATE_SCHEDULE` | [UPDATE_PAYMENT_PLAN](../api/loan-api.md#update-payment-plan) |
| `LOAN_API.DO_COM_SCHEDULE_ALLIGNMENT` | [do_commission_recognition](../api/loan-api.md#do-commission-recognition) |
| `LOAN_API.DO_DELETE_OPERATION` | [reverse_update](../api/loan-api.md#reverse-update) |
| `LOAN_API.DO_JOURNAL_ENTRY` | [evaluate_limit_amount](../api/loan-api.md#evaluate-limit-amount), [create_journal_entries](../api/loan-api.md#create-journal-entries), [do_int_calculation](../api/loan-api.md#do-int-calculation), [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation), [do_Loan_Close_With_Collateral_Out](../api/loan-api.md#do-loan-close-with-collateral-out), [create_overdrafts](../api/loan-api.md#create-overdrafts) |
| `LOAN_API.DO_PLAN_CONTROL` | [do_delete_operation](../api/loan-api.md#do-delete-operation), [update_loan_history](../api/loan-api.md#update-loan-history), [do_int_calculation](../api/loan-api.md#do-int-calculation), [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation), [create_overdrafts](../api/loan-api.md#create-overdrafts) |
| `LOAN_API.FINALIZE_ADDTIONAL_PROCESS` | [evaluate_limit_amount](../api/loan-api.md#evaluate-limit-amount), [do_int_calculation](../api/loan-api.md#do-int-calculation), [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation), [UPDATE_PAYMENT_PLAN](../api/loan-api.md#update-payment-plan) |
| `LOAN_API.GENERATE_ALLOCATED_PAYMENT_LIST` | [do_Auto_Payment](../api/loan-api.md#do-auto-payment) |
| `LOAN_API.GET_ACC_TYPE_BY_STATUS` | [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation), [UPDATE_PAYMENT_PLAN](../api/loan-api.md#update-payment-plan) |
| `LOAN_API.GET_AMOUNT_FOR_PEN_CALC` | [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.GET_DELAY_INT_RATE` | [do_Loan_Delay_Int_Rate_Upd](../api/loan-api.md#do-loan-delay-int-rate-upd) |
| `LOAN_API.GET_FORMATTED_GRACE_FROM_LIST` | [get_grace_info](../api/loan-api.md#get-grace-info) |
| `LOAN_API.GET_GL_ACC_ACTIVE_PASSIVE` | [create_loan_history](../api/loan-api.md#create-loan-history), [update_loan_history](../api/loan-api.md#update-loan-history) |
| `LOAN_API.GET_GL_ACC_FROM_MATRIX` | [create_account](../api/loan-api.md#create-account), [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.GET_GL_VALUE` | [loan_int_diff_operation](../api/loan-api.md#loan-int-diff-operation), [get_plan_error](../api/loan-api.md#get-plan-error), [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.GET_INTEREST_CALC_DATES` | [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.GET_INTEREST_CALC_INFO` | [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.GET_LOAN_AMOUNT` | [do_Auto_Payment](../api/loan-api.md#do-auto-payment) |
| `LOAN_API.GET_NEW_ACC` | [create_account](../api/loan-api.md#create-account) |
| `LOAN_API.GET_OVD_DATE` | [do_Auto_Payment](../api/loan-api.md#do-auto-payment), [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.GET_PLAN_ERROR` | [do_loan_control](../api/loan-api.md#do-loan-control-2), [UPDATE_PAYMENT_PLAN](../api/loan-api.md#update-payment-plan) |
| `LOAN_API.GET_PLAN_PAYMENT_AMOUNT` | [get_loan_amount](../api/loan-api.md#get-loan-amount), [generate_allocated_payment_list](../api/loan-api.md#generate-allocated-payment-list), [add_payment_details](../api/loan-api.md#add-payment-details) |
| `LOAN_API.GET_TRN_CALLER_ID` | [evaluate_limit_amount](../api/loan-api.md#evaluate-limit-amount), [do_int_calculation](../api/loan-api.md#do-int-calculation), [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation), [do_commission_recognition](../api/loan-api.md#do-commission-recognition), [create_overdrafts](../api/loan-api.md#create-overdrafts) |
| `LOAN_API.G_DATE_TAB_TYPE` | [get_interest_calc_dates](../api/loan-api.md#get-interest-calc-dates), [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.G_ENTRIES_LIST_TAB` | [evaluate_limit_amount](../api/loan-api.md#evaluate-limit-amount), [do_int_calculation](../api/loan-api.md#do-int-calculation), [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation), [do_Loan_Close_With_Collateral_Out](../api/loan-api.md#do-loan-close-with-collateral-out), [create_overdrafts](../api/loan-api.md#create-overdrafts) |
| `LOAN_API.G_LOAN_ACCOUNTS_REC_TYPE` | [generate_allocated_payment_list](../api/loan-api.md#generate-allocated-payment-list) |
| `LOAN_API.G_LOAN_ACCOUNTS_TAB` | [generate_allocated_payment_list](../api/loan-api.md#generate-allocated-payment-list), [add_payment_details](../api/loan-api.md#add-payment-details), [do_Auto_Payment](../api/loan-api.md#do-auto-payment), [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation) |
| `LOAN_API.LOAN_INT_DIFF_OPERATION` | [loan_int_diff_operation](../api/loan-api.md#loan-int-diff-operation), [create_loan_history](../api/loan-api.md#create-loan-history), [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `LOAN_API.REVERSE_UPDATE` | [do_delete_operation](../api/loan-api.md#do-delete-operation) |
| `LOAN_API.TABLE_LOG_OPERATION` | [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation), [UPDATE_PAYMENT_PLAN](../api/loan-api.md#update-payment-plan) |
| `LOAN_CATEGORY_API.CHANGE_OV_STATUS` | [change_account_status](../api/loan-api.md#change-account-status) |
| `LOAN_REPORT_API.GET_LOAN_MESSAGE` | [evaluate_limit_amount](../api/loan-api.md#evaluate-limit-amount), [do_int_calculation](../api/loan-api.md#do-int-calculation), [do_overdue_transit_operation](../api/loan-api.md#do-overdue-transit-operation) |
| `LOAN_TRANCHE_API.DO_CREATE_TRANCHE` | [do_create_tranche](../api/loan-api.md#do-create-tranche) |
| `LOAN_TRANCHE_API.DO_DELETE_OPERATION` | [do_delete_operation](../api/loan-api.md#do-delete-operation) |
| `LOAN_TRANCHE_API.DO_TRANCHE_OPERATION` | [do_Auto_Payment](../api/loan-api.md#do-auto-payment) |
| `LOAN_TRANCHE_API.GET_OVD_DATE` | [get_ovd_date](../api/loan-api.md#get-ovd-date), [get_ovd_date_old](../api/loan-api.md#get-ovd-date-old) |
| `LOAN_TRANCHE_API.GET_PLAN_PAYMENT_AMOUNT` | [get_plan_payment_amount](../api/loan-api.md#get-plan-payment-amount) |
| `LOAN_TRANCHE_API.G_LOAN_TRANCHE_TAB` | [finalize_addtional_process](../api/loan-api.md#finalize-addtional-process) |
| `LOAN_TRANCHE_API.OVD_AMOUNT_CORRECTION` | [update_loan_history](../api/loan-api.md#update-loan-history) |
| `LOAN_TRANCHE_API.TABLE_LOG_OPERATION` | [post_int_amount_to_plan](../api/loan-api.md#post-int-amount-to-plan) |
| `L_LOG.GET_STRING` | [reverse_update](../api/loan-api.md#reverse-update) |
| `L_OBJ.GET` | [reverse_update](../api/loan-api.md#reverse-update) |
| `L_OBJ.GET_STRING` | [get_additional_info](../api/loan-api.md#get-additional-info) |
| `L_OLD.GET_STRING` | [reverse_update](../api/loan-api.md#reverse-update) |
| `L_TRN.GET` | [reverse_update](../api/loan-api.md#reverse-update) |
| `L_TRNS.GET` | [reverse_update](../api/loan-api.md#reverse-update) |
| `MM_ACCOUNTING#.FIS_SIL` | [do_delete_operation](../api/loan-api.md#do-delete-operation) |
| `MM_ACCOUNTING#.POST_JOURNAL` | [do_journal_entry](../api/loan-api.md#do-journal-entry), [do_loan_collateral_out](../api/loan-api.md#do-loan-collateral-out) |
| `O.PARAM_ID` | [get_loan_amount](../api/loan-api.md#get-loan-amount), [generate_allocated_payment_list](../api/loan-api.md#generate-allocated-payment-list), [add_payment_details](../api/loan-api.md#add-payment-details) |
| `O.TYPE_ID` | [get_loan_amount](../api/loan-api.md#get-loan-amount), [generate_allocated_payment_list](../api/loan-api.md#generate-allocated-payment-list), [add_payment_details](../api/loan-api.md#add-payment-details) |
| `P.ACC_TYPE` | [get_loan_amount](../api/loan-api.md#get-loan-amount), [generate_allocated_payment_list](../api/loan-api.md#generate-allocated-payment-list) |
| `PA_API#.CREATE_J_WSQL` | [do_journal_entry](../api/loan-api.md#do-journal-entry), [do_loan_collateral_out](../api/loan-api.md#do-loan-collateral-out) |
| `PH_API.GET_PARAMETER` | [do_loan_collateral_out](../api/loan-api.md#do-loan-collateral-out) |
| `PR.URUN_KOD` | [do_int_calculation](../api/loan-api.md#do-int-calculation) |
| `RUHA3H.LOG` | [clear_addtional_data](../api/loan-api.md#clear-addtional-data), [add_additional_group](../api/loan-api.md#add-additional-group), [end_additional_group](../api/loan-api.md#end-additional-group), [add_additional_info](../api/loan-api.md#add-additional-info-1), [add_column_update](../api/loan-api.md#add-column-update-1) |
| `TRN_BROKER.REGISTER_EOD` | [do_journal_entry](../api/loan-api.md#do-journal-entry), [create_loan_history](../api/loan-api.md#create-loan-history), [do_loan_collateral_out](../api/loan-api.md#do-loan-collateral-out), [do_Loan_Close_With_Collateral_Out](../api/loan-api.md#do-loan-close-with-collateral-out), [UPDATE_PAYMENT_PLAN](../api/loan-api.md#update-payment-plan) |
| `TRN_BROKER.SETTXDETAILS` | [do_journal_entry](../api/loan-api.md#do-journal-entry), [do_loan_collateral_out](../api/loan-api.md#do-loan-collateral-out) |
| `TRN_BROKER.SETTXSTATE` | [do_journal_entry](../api/loan-api.md#do-journal-entry), [do_loan_collateral_out](../api/loan-api.md#do-loan-collateral-out), [do_Loan_Close_With_Collateral_Out](../api/loan-api.md#do-loan-close-with-collateral-out) |
| `TRN_BROKER.STARTTX` | [do_guarantee_out](../api/loan-api.md#do-guarantee-out), [do_non_cash_loan_close](../api/loan-api.md#do-non-cash-loan-close) |
