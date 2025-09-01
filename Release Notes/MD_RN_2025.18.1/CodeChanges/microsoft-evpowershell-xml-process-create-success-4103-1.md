# Code Changes for microsoft-evpowershell-xml-process-create-success-4103-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['<TimeCreated SystemTime=(\'|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)\\'\/>'] |
| edit_regex_field | user_sid |  | ['<Security UserID=(\'|")({user_sid}[\w-]+)(\'|")'] |