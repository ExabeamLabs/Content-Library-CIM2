# Code Changes for microsoft-sysmon-xml-service-state-modify-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | state |  | ['<Data Name\\*=(\'|")State(\'|")>({state}.+?)<\/Data>'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}.+?)(\'|")\/>'] |