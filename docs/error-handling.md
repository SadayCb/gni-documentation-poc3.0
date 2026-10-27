# Error handling — source excerpts

Errors listed here are **static code evidence**. They do not guarantee these branches will execute under a given call. The behavior of custom `R(...)` is outside the provided source.

## [post_int_amount_to_plan](api/loan-api.md#post-int-amount-to-plan)

- `when no_data_found then r(p_text => 'Account type{' || p_acc_type || '} not found, In table LOAN_ACC_TYPES_PR, only account types with has_payment_plan_yn = Y`
- `r(p_text => 'Account type{' || p_acc_type || '} not found, In table LOAN_ACC_TYPES_PR, only account types with has_payment_plan_yn = Y and acc_type_group in (INT, INT_TRS, OVD_INT, PEN) can post amounts to the plan');`
- `when others then r(p_text => 'Error encountered in search in acc_type{' || p_acc_type || '} in LOAN_ACC_TYPES_PR table!');`
- `r(p_text => 'Error encountered in search in acc_type{' || p_acc_type || '} in LOAN_ACC_TYPES_PR table!'); end;`
- `when others then r(p_text => 'Error encountered in search of main acc type with params: doc_no{' || p_doc_no || '}, tranche_no{' || p_tranche_no ||`
- `r(p_text => 'Error encountered in search of main acc type with params: doc_no{' || p_doc_no || '}, tranche_no{' || p_tranche_no || '}, plan_date{' || p_plan_date ||`
- `r(p_text => 'Posting amounts is not allowed for this account type{' || p_acc_type || '}'); end if;`
- `r(p_text => 'p_with_tranche_info_yn shoul be Y - with tranche loans, N - for standart loans!'); end if; `
- `r(p_text => 'Plan with acc_type {' || p_acc_type || '} not founc!'); end if; `

## [evaluate_limit_amount](api/loan-api.md#evaluate-limit-amount)

- `When Others Then r('doc_no: ' || m.doc_no || Chr(10) || Sqlerrm); end;`
- `r('doc_no: ' || m.doc_no || Chr(10) || Sqlerrm); end; if p_caller_tx_fid is null and p_doc_no is null then`

## [get_amount_for_pen_calc](api/loan-api.md#get-amount-for-pen-calc-1)

- `r(p_text => 'Overdue int in plan or ovd_balance amount for penalty calculation is negative!'); end if; `

## [get_ovd_trs_oper_type](api/loan-api.md#get-ovd-trs-oper-type)

- `r(p_text => 'Overdue amount {' || p_ovd_balance || '} cant be negative!'); end if;`
- `r(p_text => 'Overdue amount {' || p_balance || '} cant be negative! doc '||p_doc_no); end if; `

## [get_amount_by_range](api/loan-api.md#get-amount-by-range)

- `when no_data_found then r(p_text => 'No data found in loan_amount_range_info table!'); when too_many_rows then`
- `r(p_text => 'No data found in loan_amount_range_info table!'); when too_many_rows then r(p_text => 'Too many rows found in loan_amount_range_info table!');`
- `when too_many_rows then r(p_text => 'Too many rows found in loan_amount_range_info table!'); when others then`
- `r(p_text => 'Too many rows found in loan_amount_range_info table!'); when others then r(p_text => 'Error encountered in loan_amount_range_info table!');`
- `when others then r(p_text => 'Error encountered in loan_amount_range_info table!'); end;`
- `r(p_text => 'Error encountered in loan_amount_range_info table!'); end; `

## [get_interest_calc_info](api/loan-api.md#get-interest-calc-info)

- `r(p_text => 'Payment day cant be null, please check!'); end if; if p_trn_date > l_last_calc_date then`
- `when others then r(p_text => 'error encountered in search of interest calculation type: ' || p_int_calc_type);`
- `r(p_text => 'error encountered in search of interest calculation type: ' || p_int_calc_type); end;`
- `r(p_text => 'Transaction date cant be less than last calculation date!'); end if; `

## [get_interest_calc_dates](api/loan-api.md#get-interest-calc-dates)

- `r(p_text => 'p_int_calc_at param should be EOD or SOD!!'); end if; `
- `r(p_text => 'P_EOD_SOD param should be E - EOD or S - SOD!!'); end if; -- int calculation in eod`
- `r(p_text => 'Interest calculation should be done at EOD or SOD!!'); end if; `

## [get_interest_calc_dates_ex](api/loan-api.md#get-interest-calc-dates-ex)

- `r(p_text => 'p_int_calc_at param should be EOD or SOD!!'); end if; `
- `r(p_text => 'P_EOD_SOD param should be E - EOD or S - SOD!!'); end if; -- int calculation in eod`
- `r(p_text => 'Interest calculation should be done at EOD or SOD!!'); end if; loop`

## [add_additional_info](api/loan-api.md#add-additional-info-1)

- `r('Function usage incomplete. When using the [loan_api.add_additional_info] or [loan_api.add_column_update] procedures, you must call [loan_api.clear_addtional_data] before initiating update operations.'); end if; `

## [add_column_update](api/loan-api.md#add-column-update-1)

- `r('Function usage incomplete. When using the [loan_api.add_additional_info] or [loan_api.add_column_update] procedures, you must call [loan_api.clear_addtional_data] before initiating update operations.'); end if; `
- `when others then r('Tag [' || p_tag_name || '] not declared in [loan_history_mapping]');`
- `r('Tag [' || p_tag_name || '] not declared in [loan_history_mapping]'); end;`
- `r('Tag [' || p_tag_name || '] is [loan_history_mapping] is incorrect!'); end if;`

## [reverse_update](api/loan-api.md#reverse-update)

- `when others then r('Can not get additional info in [loan_operation_history] with tx fid [' || p_Tx_fid || ']');`
- `r('Can not get additional info in [loan_operation_history] with tx fid [' || p_Tx_fid || ']'); end;`
- `when others then l_offer_id := 'X'; --r('Can not get find loan[' || l_doc_no || '] in [krd_teklif_detay]');`

## [do_create_tranche](api/loan-api.md#do-create-tranche)

- `r('In Creation this parameteres cant be p_contract_no or p_tranche_amount null!'); end if; `
- `when others then r('Does not find loan in [krd_teklif_detay] with contract_no [' || p_contract_no || ']');`
- `r('Does not find loan in [krd_teklif_detay] with contract_no [' || p_contract_no || ']'); end;`
- `when others then r(p_text => 'Error encountered in search of tx_fid in glbl_transaction'); end;`
- `r(p_text => 'Error encountered in search of tx_fid in glbl_transaction'); end; `
- `r(p_text => 'p_trn_type should be CREATE - for create, DELETE - for delete'); end if; `
- `when others then p_tx_fid := l_tx_fid; R('Error ocured when [do_create_tranche] ' || sqlerrm);`
- `R('Error ocured when [do_create_tranche] ' || sqlerrm); end; `

## [do_delete_operation](api/loan-api.md#do-delete-operation)

- `when others then r('Can not get additional info in [loan_operation_history] with tx fid [' || p_Tx_fid || '] {l_date: ' || l_date || '}');`
- `r('Can not get additional info in [loan_operation_history] with tx fid [' || p_Tx_fid || '] {l_date: ' || l_date || '}'); end;`
- `r('Not declared delete operation [' || p_tx_fid || ']'); end if; `

## [get_loan_amount](api/loan-api.md#get-loan-amount)

- `r(p_text => 'p_amount_type should be TOTAL - All balances (Main, Int, Lim, etc.) , DEBT - The debt the customer can pay (Main, Int, etc.) DUE - Today payment amount (according to the schedule)');`
- `r(p_text => '[' || p_doc_no || '] acc_type[' || nvl(m.acc_type, m.cs_acc_type) || '] in loan_acc_types_pr or param_id in Krd_Pym_Order is null!');`

## [get_overdue_min_amount](api/loan-api.md#get-overdue-min-amount)

- `when no_data_found then r(p_text => 'Product code ' || p_product_code || ' not found in pkrd_turkod_pr table!');`
- `r(p_text => 'Product code ' || p_product_code || ' not found in pkrd_turkod_pr table!'); when others then`
- `when others then r(p_text => 'Error encountered in search of Product code ' || p_product_code || ' in pkrd_turkod_pr table!');`
- `r(p_text => 'Error encountered in search of Product code ' || p_product_code || ' in pkrd_turkod_pr table!'); end;`

## [get_overdue_grace_days](api/loan-api.md#get-overdue-grace-days)

- `when no_data_found then r(p_text => 'Product code ' || p_product_code || ' not found in pkrd_turkod_pr table!');`
- `r(p_text => 'Product code ' || p_product_code || ' not found in pkrd_turkod_pr table!'); when others then`
- `when others then r(p_text => 'Error encountered in search of Product code ' || p_product_code || ' in pkrd_turkod_pr table!');`
- `r(p_text => 'Error encountered in search of Product code ' || p_product_code || ' in pkrd_turkod_pr table!'); end;`

## [get_trn_caller_id](api/loan-api.md#get-trn-caller-id)

- `when no_data_found then r(p_text => 'Operation type ' || p_oper_type || ' not found in loan_operation_desc table!');`
- `r(p_text => 'Operation type ' || p_oper_type || ' not found in loan_operation_desc table!'); when others then`
- `when others then r(p_text => 'Error encountered in search of Operation type ' || p_oper_type || ' in loan_operation_desc table!');`
- `r(p_text => 'Error encountered in search of Operation type ' || p_oper_type || ' in loan_operation_desc table!'); end;`

## [get_voucher_data_from_query](api/loan-api.md#get-voucher-data-from-query)

- `r('p_query can be null!'); end if; `
- `r('p_result_type should be SINGLE_ROW or MULTI_ROW!'); end if; `
- `r('GROUP_CODE field is not defined in query or GROUP_CODE field is null!'); end if; `
- `r('Result of query is empty!'); elsif p_result_type = 'SINGLE_ROW' and l_col_value_tab_map.count > 1 then r('Result of query return multi row!');`
- `r('Result of query return multi row!'); end if; `
- `when others then if dbms_sql.is_open(l_cursor_id) then dbms_sql.close_cursor(l_cursor_id);`
- `r('Error encountered in query! ' || sqlerrm); raise; end;`
- `raise; end; `

## [get_formatted_grace_from_list](api/loan-api.md#get-formatted-grace-from-list)

- `r(p_text => q'(Defines grace periods for principal and interest payments using formats like '1-4' for consecutive months (1,2,3,4), '2,4,6' for specific months, or '1-4,6,9' for mixed ranges (1,2,3,4,6,9))');`

## [get_grace_info](api/loan-api.md#get-grace-info)

- `r(p_text => 'p_info_type should be HAS_GRACE - Indicates whether a grace period applies (Y/N) PERIOD - Lists the applicable months in formats like 1-4, 2,4,6, or 1-4,6,9 COUNT - Specifies the number of grace periods allowed`

## [get_basis_year_days_cnt](api/loan-api.md#get-basis-year-days-cnt)

- `when others then r(p_text => 'Error encountered in search of int calc type ' || p_int_calc_type || ' in loan_int_calc_types_pr table!');`
- `r(p_text => 'Error encountered in search of int calc type ' || p_int_calc_type || ' in loan_int_calc_types_pr table!'); end;`

## [get_gl_value](api/loan-api.md#get-gl-value)

- `when NO_DATA_FOUND then r(p_text => 'Parameter{' || p_parameter_name || '} not found in loan_global_parameters_pr table!');`
- `r(p_text => 'Parameter{' || p_parameter_name || '} not found in loan_global_parameters_pr table!'); when TOO_MANY_ROWS then`
- `when TOO_MANY_ROWS then r(p_text => 'Too many rows in search of parameter{' || p_parameter_name ||`
- `r(p_text => 'Too many rows in search of parameter{' || p_parameter_name || '} in loan_global_parameters_pr table!');`
- `when OTHERS then r(p_text => 'Encountered error in search of parameter {' || p_parameter_name ||`
- `r(p_text => 'Encountered error in search of parameter {' || p_parameter_name || '} in loan_global_parameters_pr table!');`

## [loan_int_diff_operation](api/loan-api.md#loan-int-diff-operation)

- `r(p_text => 'p_tx_fid or p_doc_no or p_acc_type or p_eod_sod cant be null!'); end if; if p_trn_type = 'INS' then`
- `r(p_text => 'original_amount or residual_amount or calc_amount or sum_residual_amount or p_plan_int_amount or p_int_amount is negative'); end if;`
- `r(p_text => 'Operation type must be INS, OPEN, CLOSE!'); end if; `

## [get_gl_acc_active_passive](api/loan-api.md#get-gl-acc-active-passive)

- `when no_data_found then r(p_text => 'Account_no: ' || p_acc_no || ' not found in gl_account_define table!');`
- `r(p_text => 'Account_no: ' || p_acc_no || ' not found in gl_account_define table!'); when too_many_rows then`
- `when too_many_rows then r(p_text => 'Encountered more than one row in gl_account_define table in search of account_no: ' ||`
- `r(p_text => 'Encountered more than one row in gl_account_define table in search of account_no: ' || p_acc_no);`
- `when others then r(p_text => 'Encountered error in gl_account_define table in search of account_no: ' ||`
- `r(p_text => 'Encountered error in gl_account_define table in search of account_no: ' || p_acc_no);`

## [get_gl_acc_from_matrix](api/loan-api.md#get-gl-acc-from-matrix)

- `r(p_text => 'p_gl_base_type should be MAIN - for main account, OVD_MAIN - for overdue account!'); end if; `
- `when others then r(p_text => 'Error encountered in search of loan_doc_no: ' || p_loan_doc_no);`
- `r(p_text => 'Error encountered in search of loan_doc_no: ' || p_loan_doc_no); end;`
- `when others then r(p_text => 'Error encountered in search krd_teklif_detay table of loan_doc_no: ' || p_loan_doc_no);`
- `r(p_text => 'Error encountered in search krd_teklif_detay table of loan_doc_no: ' || p_loan_doc_no); end;`
- `when no_data_found then r(p_text => 'No data found in gl_urun_hesap_pr table!'); when too_many_rows then`
- `r(p_text => 'No data found in gl_urun_hesap_pr table!'); when too_many_rows then r(p_text => 'Many rows found in gl_urun_hesap_pr table!');`
- `when too_many_rows then r(p_text => 'Many rows found in gl_urun_hesap_pr table!'); when others then`
- `r(p_text => 'Many rows found in gl_urun_hesap_pr table!'); when others then r(p_text => 'Error encountered in gl_urun_hesap_pr table!');`
- `when others then r(p_text => 'Error encountered in gl_urun_hesap_pr table!'); end;`
- `r(p_text => 'Error encountered in gl_urun_hesap_pr table!'); end; `
- `r(p_text => 'p_acc_type is invalid!'); end if; return l_gl_acc;`

## [Get_Delay_Int_Rate](api/loan-api.md#get-delay-int-rate)

- `When Others Then Return 0; End;`

## [get_commission_schedule](api/loan-api.md#get-commission-schedule)

- `r(p_text => gni_message.get_message('GNI_SYSTEM_VERILME_BITME_TARIX', p_begin_date, p_end_date));`
- `r(p_text => gni_message.get_message(l_mess_name => 'GNI_SYSTEM_KOMISSIYA_QRAFIK')); End If; If p_amount <= 0 Then`
- `r(p_text => gni_message.get_message(l_mess_name => 'GNI_SYSTEM_KOMISSIYA_MEBLEG')); End If; `

## [get_ovd_date](api/loan-api.md#get-ovd-date)

- `r(p_text => 'p_calc_mode should be FOR_PEN_CALC - for penalty calculation, DEFAULT-for reporting'); end if; `

## [get_ovd_date_old](api/loan-api.md#get-ovd-date-old)

- `r(p_text => 'p_calc_mode should be FOR_PEN_CALC - for penalty calculation, DEFAULT-for reporting'); end if; `

## [get_amount_for_pen_calc](api/loan-api.md#get-amount-for-pen-calc-2)

- `when too_many_rows then r(p_text => 'Too many rows in loan_special_days_pr for date: ' || p_date);`
- `r(p_text => 'Too many rows in loan_special_days_pr for date: ' || p_date); when others then`
- `when others then null; end;`
- `r(p_text => 'p_for_spec_days must be Y or N!');  end if;`

## [get_plan_paid_month_count](api/loan-api.md#get-plan-paid-month-count)

- `r('Salaaaam');  return 0;`

## [get_Pym_Startdate](api/loan-api.md#get-pym-startdate)

- `r(p_text => gni_message.get_message('GNI_SYSTEM_GET_PYM_STARTDATE_NULL', p_Doc_No)); End If;`
- `When Others Then l_Pym_Startdate := Last_Day(l_Plan_Min_Date); End;`
- `r(p_text => gni_message.get_message('GNI_SYSTEM_GET_PYM_STARTDATE_SYSDATE', p_Doc_No)); End If;`

## [get_account_feature](api/loan-api.md#get-account-feature)

- `when others then return null; end;`

## [table_log_operation](api/loan-api.md#table-log-operation)

- `r(p_text => 'p_tx_fid or p_document_no parameters cant be null!'); end if; `
- `r(p_text => 'Oper type should be LOGGING-for logging or RESTORING-for restoring'); end if; `
- `r('Function usage incomplete. When using the [loan_api.add_additional_info] or [loan_api.add_column_update] procedures, you must call [loan_api.clear_addtional_data] before initiating update operations.'); end if; `
- `r(p_text => 'Table name should be [LOAN_PAYMENT_PLAN],[LOAN_FLOW_RATIO_INFO],[LOAN_STOP_RATIO_INFO],[LOAN_CATEGORY],[KRD_KOM_PLAN_DETAY]'); end if; end;`

## [do_journal_entry](api/loan-api.md#do-journal-entry)

- `r(p_text => 'p_trn_type must be CREATE or POST!'); end if; `

## [create_journal_entries](api/loan-api.md#create-journal-entries)

- `when no_data_found then r('No data found in loan_operation_desc!'); when too_many_rows then`
- `r('No data found in loan_operation_desc!'); when too_many_rows then r('Too many rows found in loan_operation_desc!');`
- `when too_many_rows then r('Too many rows found in loan_operation_desc!'); when others then`
- `r('Too many rows found in loan_operation_desc!'); when others then r('Error encountered in loan_operation_desc!');`
- `when others then r('Error encountered in loan_operation_desc!'); end;`
- `r('Error encountered in loan_operation_desc!'); end; `
- `when others then r(' Query column: ' || l_column_name || ', with value: ' || l_column_value || ' ' || sqlerrm);`
- `r(' Query column: ' || l_column_name || ', with value: ' || l_column_value || ' ' || sqlerrm); end;`
- `when others then r('Error encountered in requirement result: ' || l_v.requirement ||`
- `r('Error encountered in requirement result: ' || l_v.requirement || ' please check requirement in loan_operation_voucher table');`
- `r('Voucher for the group_code: ' || l_col_value_tab(k).group_code || ' not found in loan_operation_voucher table'); end if;`
- `when others then l_error_msg := sqlerrm; r('In operation type: ' || p_oper_type || ' ' || l_error_msg);`

## [create_account](api/loan-api.md#create-account)

- `when others then r('Error encountered in loan table krd_teklif_detay!'); end;`
- `r('Error encountered in loan table krd_teklif_detay!'); end; `
- `When Others Then r('[' || Nvl(l_days_count, 0) || '] ' || gni_message.get_message(l_mess_name => 'GNI_2201_1_NOFTERMT'));`
- `r('[' || Nvl(l_days_count, 0) || '] ' || gni_message.get_message(l_mess_name => 'GNI_2201_1_NOFTERMT')); End;`
- `when others then r('Error ocured at Create condition - ' || sqlerrm); end;`
- `r('Error ocured at Create condition - ' || sqlerrm); end; if l_is_creation_enabled_yn = 'Y' Then`
- `r(p_text => 'Balance account for ' || m.acc_type || ' not return from loan_api.get_gl_acc_from_matrix function!'); end if;`
- `when others then -- burada exception da qoydum ele bele r('ACC_TYPE: ' || m.acc_type || ' - PRODUCT: ' ||`
- `r('ACC_TYPE: ' || m.acc_type || ' - PRODUCT: ' || l_info.urun_kod || ' - CUST_TPYE: ' || l_cust_type || ' - PERIOD_ID: ' || l_period_id || ' - CCY_ID: ' || L_curr_id ||`

## [recalculate_int_payment_plan](api/loan-api.md#recalculate-int-payment-plan)

- `r(p_text => 'p_schedule_update_type should be 3 or 4!'); end if; for m in (select k.fid,`

## [get_new_acc](api/loan-api.md#get-new-acc)

- `when others then r(gni_message.get_message('GNI_SYSTEM_DUZGUN_DEYIL', p_loan_acc_type,`
- `r(gni_message.get_message('GNI_SYSTEM_DUZGUN_DEYIL', p_loan_acc_type, p_balance_acc));`
- `r(p_text => gni_message.get_message('GNI_SYSTEM_OPEN_NEW_ACC', p_loan_doc_no, l_loan_acc_type));`
- `when others then r(gni_message.get_message('GNI_SYSTEM_OPEN_NEW_ACC_BALANCE', p_acc_description,`
- `r(gni_message.get_message('GNI_SYSTEM_OPEN_NEW_ACC_BALANCE', p_acc_description, p_balance_acc,`

## [do_plan_control](api/loan-api.md#do-plan-control)

- `r(l_err_desc); end if; end;`

## [do_loan_control](api/loan-api.md#do-loan-control-1)

- `r('Errors detected after operation [' || p_oper_type || ']. Please review the table [LOAN_EOD_CONTROL] for details.'); end if;`
- `r(p_text => 'Doc_no {' || m.sened_no || '} cs_account.account_closed_date column is not null, while krd_teklif_detay.kdate column is null!'); end loop;`

## [do_loan_status_control](api/loan-api.md#do-loan-status-control)

- `r(p_text => gni_message.get_message(l_mess_name => 'GNI_SYSTEM_KREDIT_STATUS')); elsif m.loan_status != 'WOFF' and m.loan_npl_balance != 0 then r(p_text => gni_message.get_message('GNI_SYSTEM_UMIDSIZ_SUB'));`
- `r(p_text => gni_message.get_message('GNI_SYSTEM_UMIDSIZ_SUB')); elsif m.loan_status = 'WOFF' and m.loan_balance != 0 then r(p_text => gni_message.get_message('GNI_SYSTEM_BALANS_SUB'));`
- `r(p_text => gni_message.get_message('GNI_SYSTEM_BALANS_SUB'));  elsif m.loan_status = 'NORM' and m.TOP_AMOUNT != 0 then`
- `r(p_text => gni_message.get_message('GNI_SYSTEM_NORM_STATUS'));  elsif m.loan_status in ('OVER', 'OVER60') and m.main_amount != 0 then`
- `r(p_text => gni_message.get_message('GNI_SYSTEM_OVER_STATUS')); elsif m.loan_status in ('OVER60') and m.int_amount != 0 then r(p_text => gni_message.get_message('GNI_SYSTEM_OVER_STATUS'));`
- `r(p_text => gni_message.get_message('GNI_SYSTEM_OVER_STATUS'));  end if;`
- `when others then r(p_text => 'Loan: ' || m.branch_no || '-' || m.customer_no || '-' || m.main_acc || ' ' || SQLERRM);`
- `r(p_text => 'Loan: ' || m.branch_no || '-' || m.customer_no || '-' || m.main_acc || ' ' || SQLERRM); end;`

## [create_loan_history](api/loan-api.md#create-loan-history)

- `when no_data_found then r(p_text => 'p_app_oper_code not found in loan_operation_desc table!'); when others then`
- `r(p_text => 'p_app_oper_code not found in loan_operation_desc table!'); when others then r(p_text => 'error encountered in search of oper_type');`
- `when others then r(p_text => 'error encountered in search of oper_type'); end;`
- `r(p_text => 'error encountered in search of oper_type'); end; `
- `when no_data_found then r(p_text => 'Transaction with tx_fid: ' || l_tx_fid || ' , trn_arg: ' || p_trn_type || ' , trn_date: ' ||`
- `r(p_text => 'Transaction with tx_fid: ' || l_tx_fid || ' , trn_arg: ' || p_trn_type || ' , trn_date: ' || p_trn_date || ' , trn_caller: ' || l_op.trn_caller ||`
- `when others then r(p_text => 'error encountered in search of tx_fid in glbl_transaction table!'); `
- `r(p_text => 'error encountered in search of tx_fid in glbl_transaction table!');  end;`
- `r('Procedure usage incomplete. When using a [loan_api.add_column_update] or [loan_api.add_additional_info] or [loan_api.clear_addtional_data] procedure, you must finalize your operation with [loan_api.finalize_addtional_process]. Ensur`
- `r(p_text => 'You need delete this operation(s) [' || h.tx_fids || '] before delete this operation [' || l_tx_fid || ']'); end loop;`
- `r(p_text => 'p_trn_type must be I-insert, U-update, D-delete'); end if; `
- `when others then clear_addtional_data(null); r(sqlerrm);`

## [update_loan_history](api/loan-api.md#update-loan-history)

- `r('[p_tx_fid] is null at [loan_api.update_loan_history]'); end if; `
- `when NO_DATA_FOUND then r('Can not find information in [loan_operation_history] with tx fid [' || p_tx_fid || ']!');`
- `r('Can not find information in [loan_operation_history] with tx fid [' || p_tx_fid || ']!'); when TOO_MANY_ROWS then`
- `when TOO_MANY_ROWS then r('Find duplicate information in [loan_operation_history] with tx fid [' || p_tx_fid || ']!');`
- `r('Find duplicate information in [loan_operation_history] with tx fid [' || p_tx_fid || ']!'); when others then`
- `when others then r('Error ocured [' || sqlerrm || '] find information in [loan_operation_history] with tx fid [' ||`
- `r('Error ocured [' || sqlerrm || '] find information in [loan_operation_history] with tx fid [' || p_tx_fid || ']!');`
- `when others then r('Error ocured [' || sqlerrm || '] find information in [loan_operation_desc] with oper_type [' ||`
- `r('Error ocured [' || sqlerrm || '] find information in [loan_operation_desc] with oper_type [' || l_op.OPER_TYPE || ']!');`

## [do_loan_collateral_out](api/loan-api.md#do-loan-collateral-out)

- `when others then r(p_text => sqlERRM || chr(010) || ' Teminat cixishi sehv! Sened_no: ' || p_doc_no ||`
- `r(p_text => sqlERRM || chr(010) || ' Teminat cixishi sehv! Sened_no: ' || p_doc_no || ' Teminat id: ' || m.tem_fid || ' Teminat Tip: ' ||`

## [get_acc_type_by_status](api/loan-api.md#get-acc-type-by-status)

- `when NO_DATA_FOUND then r('Can not find acc type [' || p_acc_type || '] in [loan_acc_type_mapping], To Loan Status - [' ||`
- `r('Can not find acc type [' || p_acc_type || '] in [loan_acc_type_mapping], To Loan Status - [' || p_to_loan_status || '], From Loan Status [' || p_from_loan_status || ']');`
- `when others then r('Something went wrong in [loan_acc_type_mapping], Acc Type [' || p_acc_type || ', To Loan Status - [' || p_to_loan_status ||`
- `r('Something went wrong in [loan_acc_type_mapping], Acc Type [' || p_acc_type || ', To Loan Status - [' || p_to_loan_status || '], From Loan Status [' || p_from_loan_status || ']');`

## [generate_allocated_payment_list](api/loan-api.md#generate-allocated-payment-list)

- `r(p_text => '[' || p_doc_no || '] acc_type[' || m.cs_acc_type || '] in loan_acc_types_pr or param_id in Krd_Pym_Order is null!'); end if;`
- `r(p_text => 'Payment branch or customer or account is null Pymt_branch_no: ' || m.pymt_branch_no || ', Pymt_customer_no: ' || m.pymt_customer_no || ', Pymt_account_no: ' ||`
- `r(p_text => 'Payment amount cant be more than balance amount! Please check amount of acc_type: ' || l_loan_accounts(j).acc_type || ' in payment plan and balance of account ' || l_loan_accounts(j).branch_no || '-' || l_loan_accounts(j).`
- `r(p_text => 'Payment amount cant be negative!'); end if; p_has_schedule_upd_type := l_has_schedule_upd_type;`

## [add_payment_details](api/loan-api.md#add-payment-details)

- `when others then r(p_text => 'Can not find Acc_type : {' || p_payment_list(j).acc_type || ':' || p_payment_list(j).pymt_amount || '} in payment list . Check [cs_acconunt] - {' ||`
- `r(p_text => 'Can not find Acc_type : {' || p_payment_list(j).acc_type || ':' || p_payment_list(j).pymt_amount || '} in payment list . Check [cs_acconunt] - {' || sqlerrm || '}');`
- `r(p_text => 'Acc_type: ' || p_payment_list(j).acc_type || ', not declared in [krd_pym_order]! '); end if;`
- `r(p_text => 'Acc_type: ' || p_payment_list(j).acc_type || ', Payment amount:(' || l_loan_accounts_rec.pymt_amount ||`
- `r(p_text => 'Acc_type: ' || p_payment_list(j).acc_type || ' Payment amount(' || l_loan_accounts_rec.pymt_amount || ') > balance amount(' || l_loan_accounts_rec.balance ||`
- `r(p_text => 'Payment branch or customer or account is null Pymt_branch_no: ' || l_loan_accounts_rec.pymt_branch_no || ', Pymt_customer_no: ' ||`

## [do_Auto_Payment](api/loan-api.md#do-auto-payment)

- `r(p_text => 'Auto payment type should be 1-Plan payment or 2-Off plan payment!'); end if; `
- `When Others Then rollback; gni_utility.log_batch_error(p_tx_fid        => l_Tx_Fid,`

## [do_int_calculation](api/loan-api.md#do-int-calculation)

- `r(p_text => 'Int calculation has not finished yet for loans without transit process!'); end if; `
- `r(p_text => 'is_int_calc or is_pen_calc columns in krd_teklif_detay table is null! Please check...'); end if; `
- `r(p_text => 'Product code not found in pkrd_turkod_pr table, pls check 22401 app for this loan product!' || m.loan_product_code);`
- `r(p_text => 'Not working day may be 1 or 2, please check 22401 app, for product code:' || m.loan_product_code);`
- `r(p_text => 'The maximum penalty amount listed for this product ' || m.loan_product_code || ' on screen 22401 cannot be 0!');`
- `r(p_text => 'Non calculated days of loan {' || m.doc_no || '} more than ' ||`
- `when others then l_has_stop_operation := 'N'; end;`
- `r(p_text => 'No data found in loan_acc_types_pr tables for account type: ' || nn.acc_type); end if;`
- `r(p_text => 'Counter account for acc_type: ' || nn.acc_type || ' not found! Check loan_api.get_gl_acc_from_matrix with param attributes: p_base_type: ' || case`
- `when no_data_found then r(p_text => 'No data found in loan_flow_ratio_info table, for date: ' || l_dates(i));`
- `r(p_text => 'No data found in loan_flow_ratio_info table, for date: ' || l_dates(i)); when too_many_rows then`
- `when too_many_rows then r(p_text => 'Too many rows found in loan_flow_ratio_info table, for date: ' || l_dates(i));`

## [do_overdue_transit_operation](api/loan-api.md#do-overdue-transit-operation)

- `r(p_text => 'Loan product code not found in pkrd_turkod_pr table!'); end if; `
- `when others then rollback; gni_utility.log_batch_error(p_tx_fid        => l_tx_fid,`

## [do_commission_recognition](api/loan-api.md#do-commission-recognition)

- `r(p_text => 'This Program can run only last day of month!'); End If; `
- `r(p_text => t.Sube_Kod || '-' || t.Musteri_No || '-' || t.Kredi_Hesap_No || ' Mushterinin qrafikinde sehv var!'); End Loop;`
- `r(p_text => Ww.Sube_Kod || '-' || Ww.Musteri_No || '-' || Ww.Kredi_Hesap_No || ' Odenilmeli mebleg 0-dan az ola bilmez!');`

## [do_guarantee_out](api/loan-api.md#do-guarantee-out)

- `When Others Then r(p_text => 'Loan acc: ' || m.Sube_Kod || '-' || m.Musteri_No || '-' || m.Kredi_Hesap_No || Chr(10) || Sqlerrm);`
- `r(p_text => 'Loan acc: ' || m.Sube_Kod || '-' || m.Musteri_No || '-' || m.Kredi_Hesap_No || Chr(10) || Sqlerrm); End;`

## [do_Loan_Close_With_Collateral_Out](api/loan-api.md#do-loan-close-with-collateral-out)

- `when others then r(p_text => 'Lim: ' || sqlerrm); end;`
- `r(p_text => 'Lim: ' || sqlerrm); end; end if;`
- `When Others Then r(p_text => 'Error: ' || i.Branch_No || '-' || i.Customer_No || '-' || i.main_Acc || Chr(10) || Sqlerrm);`
- `r(p_text => 'Error: ' || i.Branch_No || '-' || i.Customer_No || '-' || i.main_Acc || Chr(10) || Sqlerrm); End;`

## [do_non_cash_loan_close](api/loan-api.md#do-non-cash-loan-close)

- `When Others Then r('Kreditde sehv: ' || m.Sube_Kod || '-' || m.Musteri_No || '-' || m.Kredi_Hesap_No || Chr(10) || Sqlerrm);`
- `r('Kreditde sehv: ' || m.Sube_Kod || '-' || m.Musteri_No || '-' || m.Kredi_Hesap_No || Chr(10) || Sqlerrm); End;`

## [do_journal_control](api/loan-api.md#do-journal-control)

- `r(p_text => '???????? ?? ????. ?????? ????? ???? ?????? ?? ?????????? ?????? !!!'); end if; end;`

## [do_schedule_allignment](api/loan-api.md#do-schedule-allignment)

- `r('at [do_schedule_allignment] parametr [p_payment_amount] less than [0]'); End If; `

## [do_com_schedule_allignment](api/loan-api.md#do-com-schedule-allignment)

- `When No_Data_Found Then Glog.Assert#(False, g_Mesg('KREDI_HESAPNO_EKNO', p_doc_no),`

## [do_Loan_Delay_Int_Rate_Upd](api/loan-api.md#do-loan-delay-int-rate-upd)

- `r(p_text => 'Gecikme Faizi 0-dan ferqli oldugu halda son gecikme faizi 0-dir!'); End If; `
- `When Others Then r(p_text => 'Kreditde sehv: ' || m.Branch_Id || '-' || m.Account_No || '-' || m.Kredi_Hesap_No || Chr(10) ||`
- `r(p_text => 'Kreditde sehv: ' || m.Branch_Id || '-' || m.Account_No || '-' || m.Kredi_Hesap_No || Chr(10) || Sqlerrm);`

## [change_account_status](api/loan-api.md#change-account-status)

- `when no_data_found then r(p_text => 'Loan with doc_no: ' || p_doc_no || ' not found!'); when others then`
- `r(p_text => 'Loan with doc_no: ' || p_doc_no || ' not found!'); when others then r(p_text => 'Error encountered in search of loan: ' || p_doc_no);`
- `when others then r(p_text => 'Error encountered in search of loan: ' || p_doc_no); end;`
- `r(p_text => 'Error encountered in search of loan: ' || p_doc_no); end; `
- `r(p_text => 'Only followings p_status are accepted O-open, C-close!'); end if; end loop;`

## [get_special_schedule](api/loan-api.md#get-special-schedule)

- `When Others Then l_annuity_amount := l_remain_amount * (1 + p_int_ratio) / l_main_pay_months;`

## [get_created_schedule](api/loan-api.md#get-created-schedule)

- `WHEN NO_DATA_FOUND THEN R('No record found for fid = ' || p_fid); end;`
- `R('No record found for fid = ' || p_fid); end; `

## [create_overdrafts](api/loan-api.md#create-overdrafts)

- `r(p_text => 'p_oper_type should be CREATE_OVERDRAFT or CLOSE_LOAN'); end if; --------------- Borcu baglanmish OV-in evvelki sublarini acmaq ------------------`
- `When Others Then r('doc_no: ' || n.sened_no || Chr(10) || Sqlerrm); end;`
- `r('doc_no: ' || n.sened_no || Chr(10) || Sqlerrm); end; end loop;`
- `When Others Then r('cust_no: ' || m.customer || Chr(10) || Sqlerrm); end;`
- `r('cust_no: ' || m.customer || Chr(10) || Sqlerrm); end; end loop;`

## [get_new_ov_cont_no](api/loan-api.md#get-new-ov-cont-no)

- `when no_data_found then r('Musteri hesabi tapilmadi!'); when others then`
- `r('Musteri hesabi tapilmadi!'); when others then r('Musteri melumatlarinda sehv var!');`
- `when others then r('Musteri melumatlarinda sehv var!'); end;`
- `r('Musteri melumatlarinda sehv var!'); end; `

## [init_global_variables](api/loan-api.md#init-global-variables)

- `raise finalize; end if; `
- `when others then r('[krd_teklif_detay] is invalid'); end;`
- `r('[krd_teklif_detay] is invalid'); end; `
- `when others then r('[krd_teklif] is invalid'); end;`
- `r('[krd_teklif] is invalid'); end; `
- `when others then r('[krd_tesis] is invalid'); end;`
- `r('[krd_tesis] is invalid'); end; `
- `when others then r('[krd_odeme_plan] is invalid'); end;`
- `r('[krd_odeme_plan] is invalid'); end; end if;`
- `when others then G_KTD := null; G_KTE := null;`
- `raise finalize; end; `

## [UPDATE_PAYMENT_PLAN](api/loan-api.md#update-payment-plan)

- `r('This operation cannot be initialized when [with_tranche_info_yn] = ''Y'''); end if; `
- `gaia.r(l_err_desc); end if; `
- `when others then  r('Update payment plan block -> ' || sqlerrm || ' - ' || dbms_utility.format_error_backtrace);`
- `r('Update payment plan block -> ' || sqlerrm || ' - ' || dbms_utility.format_error_backtrace); END;--Nicat `
