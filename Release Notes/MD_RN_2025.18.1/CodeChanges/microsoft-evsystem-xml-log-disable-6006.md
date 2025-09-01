# Code Changes for microsoft-evsystem-xml-log-disable-6006 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_id |  | ['ProcessID\\*=(\'|")({process_id}\d+)'] |
| edit_regex_field | thread_id |  | ['ThreadID\\*=(\'|")({thread_id}[^\'"]+)'] |