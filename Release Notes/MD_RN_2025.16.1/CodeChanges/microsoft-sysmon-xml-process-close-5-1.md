# Code Changes for microsoft-sysmon-xml-process-close-5-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/<]+?))<\/Data>'] |
| edit_regex_field | process_guid |  | ['<Data Name\\*=(\'|")ProcessGuid(\'|")>\{({process_guid}[^\}]+)'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")ProcessId(\'|")>({process_id}.+?)<\/Data>'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/<]+?))<\/Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/<]+?))<\/Data>'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}.+?)(\'|")\/>'] |