# Code Changes for microsoft-evsecurity-json-service-create-success-4697 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['"EventID":4697', '"ServiceFileName":"', '"ServiceName":"', '"ServiceStartType":"'] |
| changed_parsed_fields | N/A |  | ['account_domain', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'operation_type', 'process_id', 'result', 'service_command_line', 'service_name', 'service_start_type', 'service_type', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_name |  | ['({event_name}A service was installed in the system)', 'exa_regex=({event_name}A service was installed in the system)'] |
| removed_regex_field | process_dir |  | [] |
| removed_regex_field | process_name |  | [] |
| removed_regex_field | process_path |  | [] |
| added_regex_field | service_command_line |  | ['"ServiceFileName":"({service_command_line}.*?)"'] |
| added_attribute | ExtractionType |  | json |