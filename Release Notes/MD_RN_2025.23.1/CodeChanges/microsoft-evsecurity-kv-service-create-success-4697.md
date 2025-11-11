# Code Changes for microsoft-evsecurity-kv-service-create-success-4697 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'result', 'service_command_line', 'service_name', 'service_start_type', 'service_type', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s)', '\sComputerName=(|({dest_host}({host}[\w\-.]+?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | process_command_line |  | ['Service File Name:\s*((?-i)\\+[rnt]\\*)*({service_command_line}({process_command_line}[^=]+?))\s*(\\t|\\r|\\n)*Service Type:'] |
| added_regex_field | dest_host |  | ['Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s)', '\sComputerName=(|({dest_host}({host}[\w\-.]+?)))(\s+\w+=|\s*$)'] |
| added_regex_field | service_command_line |  | ['Service File Name:\s*((?-i)\\+[rnt]\\*)*({service_command_line}({process_command_line}[^=]+?))\s*(\\t|\\r|\\n)*Service Type:'] |
| removed_attribute | DupFields |  | N/A |