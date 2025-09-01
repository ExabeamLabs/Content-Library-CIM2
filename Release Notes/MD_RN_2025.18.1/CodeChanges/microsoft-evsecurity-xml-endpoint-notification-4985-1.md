# Code Changes for microsoft-evsecurity-xml-endpoint-notification-4985-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_guid |  | ['Guid\\*=(\'|")\{({process_guid}[^\\'\}]+)'] |
| edit_regex_field | thread_id |  | ['ThreadID(\\)?=(\'|")({thread_id}\d+)'] |