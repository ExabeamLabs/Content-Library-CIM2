# Code Changes for microsoft-evsecurity-xml-group-modify-success-4750 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | group_id |  | ['<Data Name=(\'|")TargetSid(\'|")>({group_id}[^<]+)'] |