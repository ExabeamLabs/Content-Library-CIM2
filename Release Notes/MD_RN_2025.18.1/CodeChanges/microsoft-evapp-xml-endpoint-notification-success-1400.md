# Code Changes for microsoft-evapp-xml-endpoint-notification-success-1400 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | additional_info |  | ['<Data Name\\*=(\'|")string0(\'|")>({additional_info}[^<]+)<'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")\/>', '<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")\/>', '<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^<\'"]+)', '<Security UserID\\*=(\'|")({user_sid}[^<\'"]+)'] |