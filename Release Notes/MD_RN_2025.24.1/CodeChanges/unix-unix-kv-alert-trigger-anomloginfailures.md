# Code Changes for unix-unix-kv-alert-trigger-anomloginfailures (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'account_name', 'alert_name', 'alert_type', 'host', 'host_ip', 'process_dir', 'process_id', 'process_name', 'session_id', 'src_host', 'time', 'user_id'] |
| edit_regex_field | alert_name |  | ['({alert_type}({alert_name}ANOM_LOGIN_FAILURES))'] |
| added_regex_field | alert_type |  | ['({alert_type}({alert_name}ANOM_LOGIN_FAILURES))'] |
| removed_attribute | DupFields |  | N/A |