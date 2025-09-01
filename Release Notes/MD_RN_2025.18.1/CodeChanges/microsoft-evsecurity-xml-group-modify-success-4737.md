# Code Changes for microsoft-evsecurity-xml-group-modify-success-4737 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | group_id |  | ['<Data Name\\?=(\'|")TargetSid(\'|")>({group_id}[^<]+)'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)'] |