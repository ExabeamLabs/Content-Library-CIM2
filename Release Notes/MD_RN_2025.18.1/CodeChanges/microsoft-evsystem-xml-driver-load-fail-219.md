# Code Changes for microsoft-evsystem-xml-driver-load-fail-219 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}[^"\']+)'] |
| edit_regex_field | thread_id |  | ['ThreadID\\*=(\'|")({thread_id}[^\'"]+)'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\'"]+)', 'User SID:\s*({user_sid}[^\s]+)'] |