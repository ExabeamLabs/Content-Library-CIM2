# Code Changes for microsoft-evsecurity-kv-service-create-success-4697-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'service_command_line', 'service_name', 'service_start_type', 'service_type', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['\sComputer_name:({dest_host}({host}[\w\-.]+))\s'] |
| edit_regex_field | process_command_line |  | ['\sService File Name:\s*((?-i)\\+[rnt]\\*)*({service_command_line}({process_command_line}[^=]+?))(\s|\\[rnt])+Service Type:'] |
| added_regex_field | dest_host |  | ['\sComputer_name:({dest_host}({host}[\w\-.]+))\s'] |
| added_regex_field | service_command_line |  | ['\sService File Name:\s*((?-i)\\+[rnt]\\*)*({service_command_line}({process_command_line}[^=]+?))(\s|\\[rnt])+Service Type:'] |
| removed_attribute | DupFields |  | N/A |