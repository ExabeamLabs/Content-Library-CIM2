# Code Changes for microsoft-evsystem-json-service-create-success-7045 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_host', 'event_code', 'event_name', 'host', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'service_command_line', 'service_name', 'service_type', 'time', 'user_sid'] |
| edit_regex_field | host |  | ['"ComputerName":"({dest_host}({host}[\w\-.]+))"', '"Hostname":"({dest_host}({host}[\w\-.]+))"'] |
| edit_regex_field | process_command_line |  | ['Service File Name:\s*({service_command_line}({process_command_line}[^=]+?))\s*(\\t|\\r|\\n)*Service Type:'] |
| added_regex_field | dest_host |  | ['"ComputerName":"({dest_host}({host}[\w\-.]+))"', '"Hostname":"({dest_host}({host}[\w\-.]+))"'] |
| added_regex_field | service_command_line |  | ['Service File Name:\s*({service_command_line}({process_command_line}[^=]+?))\s*(\\t|\\r|\\n)*Service Type:'] |
| removed_attribute | DupFields |  | N/A |