# Code Changes for microsoft-sysmon-xml-file-write-success-11 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | file_dir |  | ['<Data Name\\*=(\'|")TargetFilename(\'|")>({file_path}(({file_dir}[^<>]+?)[\\\/]+)?\s*({file_name}[^\\\/<>]*?(\.({file_ext}\w+))?))<\/Data>'] |
| edit_regex_field | file_ext |  | ['<Data Name\\*=(\'|")TargetFilename(\'|")>({file_path}(({file_dir}[^<>]+?)[\\\/]+)?\s*({file_name}[^\\\/<>]*?(\.({file_ext}\w+))?))<\/Data>'] |
| edit_regex_field | file_name |  | ['<Data Name\\*=(\'|")TargetFilename(\'|")>({file_path}(({file_dir}[^<>]+?)[\\\/]+)?\s*({file_name}[^\\\/<>]*?(\.({file_ext}\w+))?))<\/Data>'] |
| edit_regex_field | file_path |  | ['<Data Name\\*=(\'|")TargetFilename(\'|")>({file_path}(({file_dir}[^<>]+?)[\\\/]+)?\s*({file_name}[^\\\/<>]*?(\.({file_ext}\w+))?))<\/Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?))<\/Data>'] |
| edit_regex_field | process_guid |  | ['<Data Name\\*=(\'|")ProcessGuid(\'|")>\{({process_guid}.+?)\}<\/Data>', '<Provider Name\\*=(\'|")Microsoft-Windows-Sysmon(\'|") Guid=(\'|")\{({process_guid}[^}]+?)\}'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")ProcessId(\'|")>({process_id}\d+)', '<Execution ProcessID\\*=(\'|")({process_id}\d+)'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?))<\/Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?))<\/Data>'] |
| edit_regex_field | time |  | ['<Data Name\\*=(\'|")UtcTime(\'|")>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)', '<TimeCreated SystemTime=(\'|")({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d.\d+Z)'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")'] |