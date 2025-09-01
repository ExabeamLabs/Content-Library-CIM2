# Code Changes for microsoft-evsecurity-xml-endpoint-notification-5033-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_guid |  | ['Guid\\*=(\'|")\{({process_guid}[^\\'\}]+)'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}[^"\']+)'] |
| edit_regex_field | thread_id |  | ['ThreadID\\*=(\'|")({thread_id}[^\'"]+)'] |