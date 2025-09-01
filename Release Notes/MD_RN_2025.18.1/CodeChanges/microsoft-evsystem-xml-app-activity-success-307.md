# Code Changes for microsoft-evsystem-xml-app-activity-success-307 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|")'] |
| edit_regex_field | time |  | ['<TimeCreated SystemTime\\*=(\'|")({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{1,10}Z)(\'|")/>'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}\S+)(\'|")/>'] |