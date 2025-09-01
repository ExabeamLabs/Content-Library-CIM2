# Code Changes for microsoft-evpowershell-xml-process-create-success-4103 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)', 'exa_regex=<Execution ProcessID\\*=(\'|")({process_id}\d+)'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[\w\-]+)(\'|")/>', 'exa_regex=<Security UserID\\*=(\'|")({user_sid}[\w\-]+)(\'|")/>'] |