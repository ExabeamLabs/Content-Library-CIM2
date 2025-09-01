# Code Changes for windows-evsystem-xml-endpoint-notification-12 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|")'] |
| edit_regex_field | thread_id |  | ['ThreadID\\*=(\'|")({thread_id}\d+)(\'|")'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")'] |