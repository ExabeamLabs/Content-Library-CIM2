# Code Changes for microsoft-sysmon-xml-dll-load-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | thread_id |  | ['ThreadID(\\)?=(\'|")({thread_id}\d+)'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}.+?)(\'|")\/>'] |