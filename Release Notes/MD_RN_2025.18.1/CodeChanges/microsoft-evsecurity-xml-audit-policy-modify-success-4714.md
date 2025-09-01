# Code Changes for microsoft-evsecurity-xml-audit-policy-modify-success-4714 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | activity_id |  | ['<Correlation ActivityID\\*=(\'|")\{({activity_id}[^\}\'"]+)'] |
| edit_regex_field | operation |  | ['<Data Name\\*=(\'|")ChangeType(\'|")>({operation}[^<]+)</Data>'] |
| edit_regex_field | process_guid |  | ['Guid\\*=(\'|")\{({process_guid}[^\\'\}]+)'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)'] |