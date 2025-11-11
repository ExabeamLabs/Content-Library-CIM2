# Code Changes for microsoft-windows-json-service-create-success-4697 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'event_code', 'event_name', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'service_command_line', 'service_name'] |
| edit_regex_field | process_command_line |  | ['exa_regex=Service File Name:\s*({service_command_line}({process_command_line}[^=]+?))\s*(\\t|\\r|\\n)*Service Type:'] |
| added_regex_field | service_command_line |  | ['exa_regex=Service File Name:\s*({service_command_line}({process_command_line}[^=]+?))\s*(\\t|\\r|\\n)*Service Type:'] |
| removed_attribute | DupFields |  | N/A |