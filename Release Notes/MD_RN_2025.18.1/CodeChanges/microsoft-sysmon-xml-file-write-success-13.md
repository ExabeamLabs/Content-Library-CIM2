# Code Changes for microsoft-sysmon-xml-file-write-success-13 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_guid |  | ['<Data Name\\*=(\'|")ProcessGuid(\'|")>\{({process_guid}.+?)\}<\/Data>', '<Provider Name\\*=(\'|")Microsoft-Windows-Sysmon(\'|") Guid=(\'|")\{({process_guid}[^}]+?)\}'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")ProcessId(\'|")>({process_id}\d+)', '<Execution ProcessID\\*=(\'|")({process_id}\d+)'] |
| edit_regex_field | time |  | ['<Data Name\\*=(\'|")UtcTime(\'|")>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)', '<TimeCreated SystemTime=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{9}Z)'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")//?>'] |