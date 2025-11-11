# Code Changes for microsoft-evsecurity-kv-alert-trigger-success-4649 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_type', 'auth_package', 'auth_process', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'time', 'user', 'user_sid'] |
| edit_regex_field | auth_process |  | ['Logon Process:\s+({alert_type}({auth_process}[^\s]+))'] |
| edit_regex_field | event_name |  | ['Message=({alert_name}({event_name}[^:]+?))\s+\w+:'] |
| added_regex_field | alert_name |  | ['Message=({alert_name}({event_name}[^:]+?))\s+\w+:'] |
| added_regex_field | alert_type |  | ['Logon Process:\s+({alert_type}({auth_process}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |