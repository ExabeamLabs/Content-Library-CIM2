# Code Changes for microsoft-evsetup-xml-app-activity-setup-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_name |  | ['<Data Name=(\'|")UpdateTitle(\'|")>"({event_name}[^"<]+)'] |
| edit_regex_field | failure_code |  | ['<Data Name=(\'|")ErrorCode(\'|")>({failure_code}[^<]+)<'] |
| edit_regex_field | process_command_line |  | ['<Data Name=(\'|")CommandLine(\'|")>({process_command_line}.+?)\s*</Data>'] |
| edit_regex_field | process_guid |  | ['Guid=(\'|")\{({process_guid}[^\}\'"]+?)\}(\'|")'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID=(\'|")({process_id}\d+)(\'|") ThreadID=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | provider_name |  | ['<Provider Name=(\'|")({provider_name}[^\'"]+)(\'|")'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID=(\'|")({process_id}\d+)(\'|") ThreadID=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | user_sid |  | ['<Security UserID=(\'|")({user_sid}[^\'"]+)(\'|")\/>'] |