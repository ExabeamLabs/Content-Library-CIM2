# Code Changes for microsoft-windows-kv-process-create-success-started (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'event_name', 'host', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'time'] |
| edit_regex_field | host |  | ['"(?i)HostName":\s*"({dest_host}({host}[\w\-.]+))"', '({dest_host}({host}[\w.\-]+)) Provider Lifecycle', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+[+-]\d+:\d+)\s*({dest_host}({host}[\w\-.]+))\s*', '\sComputerName=(|({dest_host}({host}[\w\-.]+?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+[+-]\d+:\d+)\s*({dest_host}({host}[\w\-.]+))\s*', 'EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"', 'Windows PowerShell\s+\S+\s+({time}\w+ \w+ \d\d \d\d:\d\d:\d\d \d\d\d\d)\s+({event_code}\d+)'] |
| added_regex_field | dest_host |  | ['"(?i)HostName":\s*"({dest_host}({host}[\w\-.]+))"', '({dest_host}({host}[\w.\-]+)) Provider Lifecycle', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+[+-]\d+:\d+)\s*({dest_host}({host}[\w\-.]+))\s*', '\sComputerName=(|({dest_host}({host}[\w\-.]+?)))(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |