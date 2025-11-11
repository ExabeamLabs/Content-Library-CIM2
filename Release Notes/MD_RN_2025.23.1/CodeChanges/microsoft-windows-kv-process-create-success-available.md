# Code Changes for microsoft-windows-kv-process-create-success-available (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'dest_host', 'event_code', 'event_name', 'host', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'time'] |
| edit_regex_field | host |  | ['"(?i)HostName":\s*"({dest_host}({host}[\w\-.]+))"', '({dest_host}({host}[\w.\-]+))\s+Engine Lifecycle', '\sComputerName=(|({dest_host}({host}[\w\-.]+?)))(\s+\w+=|\s*$)'] |
| added_regex_field | dest_host |  | ['"(?i)HostName":\s*"({dest_host}({host}[\w\-.]+))"', '({dest_host}({host}[\w.\-]+))\s+Engine Lifecycle', '\sComputerName=(|({dest_host}({host}[\w\-.]+?)))(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |