# Code Changes for microsoft-evsystem-str-service-create-success-7045 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'dest_host', 'dest_ip', 'domain', 'event_code', 'event_name', 'host', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'service_command_line', 'service_name', 'service_type', 'time', 'user'] |
| edit_regex_field | process_command_line |  | ['Service File Name:\s*({service_command_line}({process_command_line}[^=]+?))\s*(\\t|\\r|\\n)*Service Type:'] |
| added_regex_field | service_command_line |  | ['Service File Name:\s*({service_command_line}({process_command_line}[^=]+?))\s*(\\t|\\r|\\n)*Service Type:'] |
| removed_attribute | DupFields |  | N/A |