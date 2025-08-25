# Code Changes for microsoft-sysmon-xml-file-write-success-11-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Security UserID\\*=(\'|")(({domain}[^\\>]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\'|")\s*/>'] |
| edit_regex_field | process_guid |  | ['<Provider Name\\*=(\'|")Microsoft-Windows-Sysmon(\'|") Guid=(\'|")\{({process_guid}[^}]+?)\}'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)'] |
| edit_regex_field | user |  | ['<Security UserID\\*=(\'|")(({domain}[^\\>]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\'|")\s*/>'] |