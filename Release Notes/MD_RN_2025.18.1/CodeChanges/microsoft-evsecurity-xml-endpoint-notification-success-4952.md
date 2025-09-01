# Code Changes for microsoft-evsecurity-xml-endpoint-notification-success-4952 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | rule |  | ['<Data Name\\*=(\'|")RuleName(\'|")>({rule}[^<]+)'] |
| edit_regex_field | rule_id |  | ['<Data Name\\*=(\'|")RuleId(\'|")>({rule_id}[^<]+)'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")\/>'] |