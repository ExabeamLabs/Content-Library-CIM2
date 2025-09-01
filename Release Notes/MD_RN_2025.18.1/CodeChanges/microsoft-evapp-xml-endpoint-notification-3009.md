# Code Changes for microsoft-evapp-xml-endpoint-notification-3009 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | activity_id |  | ['<Correlation ActivityID\\*=(\'|")\{({activity_id}[^\}\'"]+)', 'ActivityID=(\'|")\{?({activity_id}[^\}\'"]+)'] |
| edit_regex_field | failure_reason |  | ['<Data Name\\*=(\'|")ErrorDescription(\'|")>({failure_reason}[^<]+?)\s*</Data>'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}[^"\']+)', 'ProcessID\\*=(\'|")({process_id}\d+)'] |
| edit_regex_field | rule |  | ['<Data Name\\*=(\'|")RuleName(\'|")>({rule}[^<]+)'] |
| edit_regex_field | rule_id |  | ['<Data Name\\*=(\'|")RuleId(\'|")>\{?({rule_id}[^}<]+)'] |
| edit_regex_field | thread_id |  | ['ThreadID\\*=(\'|")({thread_id}[^\'"]+)'] |