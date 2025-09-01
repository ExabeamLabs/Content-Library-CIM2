# Code Changes for microsoft-evsecurity-kv-log-clear-success-logfileclear (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_id |  | ['<Execution ProcessID(\\)?=(\'|")({process_id}[^"\']+)', '<Execution ProcessID\\*=(\'|")({process_id}[^"\']+)'] |
| edit_regex_field | thread_id |  | ['ThreadID\\*=(\'|")({thread_id}\d+)'] |
| edit_regex_field | time |  | ['SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\d\d\dZ)'] |