# Code Changes for microsoft-azuresc-json-alert-trigger-success-security (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'process_name', 'time', 'user', 'user_sid'] | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'process_dir', 'process_name', 'process_path', 'time', 'user', 'user_sid'] |
| edit_regex_field | process_name | ['"processName":"({process_name}[^"]+)"'] | ['"processName":"({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"'] |
| added_regex_field | process_dir | [] | ['"processName":"({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"'] |
| added_regex_field | process_path | [] | ['"processName":"({process_path}({process_dir}[^"]*[\\\/]+)?({process_name}[^"]+?))"'] |