# Code Changes for microsoft-evsecurity-xml-endpoint-notification-success-5446 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_guid |  | ['Guid\\*=(\'|")\{({process_guid}[^\\'\}]+)'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")ProcessId(\'|")>({process_id}[^<]+)<', '<Execution ProcessID\\*=(\'|")({process_id}\d+)'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")UserSid(\'|")>({user_sid}[^<]+)<'] |