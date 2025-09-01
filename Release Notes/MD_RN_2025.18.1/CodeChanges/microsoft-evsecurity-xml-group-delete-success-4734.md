# Code Changes for microsoft-evsecurity-xml-group-delete-success-4734 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_id |  | ['<Execution ProcessID(\\)?=(\'|")({process_id}\d+)(\'|") ThreadID(\\)?=(\'|")({thread_id}\d+)(\'|")'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID(\\)?=(\'|")({process_id}\d+)(\'|") ThreadID(\\)?=(\'|")({thread_id}\d+)(\'|")'] |