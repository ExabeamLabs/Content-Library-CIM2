# Code Changes for microsoft-sysmon-xml-process-create-success-processcreate-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_process_id |  | ['(?i)<Data Name\\*=(\'|")TargetProcessGuid(\'|")>\{({dest_process_id}[A-F0-9a-f-]+)\}</Data>', '<Data Name\\*=(\'|")TargetProcessId(\'|")>({dest_process_id}\d+)</Data>'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")User(\'|")>(({domain}[^\\<]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | hash_md5 |  | ['<Data Name\\*=(\'|")Hashes(\'|")>.*?MD5=({hash_md5}[A-F0-9a-f]+).*?</Data>'] |
| edit_regex_field | parent_process_dir |  | ['<Data Name\\*=(\'|")SourceImage(\'|")>({parent_process_path}(({parent_process_dir}[^<]*)\\+)?({parent_process_name}[^<]+?))</Data>'] |
| edit_regex_field | parent_process_name |  | ['<Data Name\\*=(\'|")SourceImage(\'|")>({parent_process_path}(({parent_process_dir}[^<]*)\\+)?({parent_process_name}[^<]+?))</Data>'] |
| edit_regex_field | parent_process_path |  | ['<Data Name\\*=(\'|")SourceImage(\'|")>({parent_process_path}(({parent_process_dir}[^<]*)\\+)?({parent_process_name}[^<]+?))</Data>'] |
| edit_regex_field | process_command_line |  | ['<Data Name\\*=(\'|")CommandLine(\'|")>({process_command_line}[^<]+?)\s*</Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")TargetImage(\'|")>({process_path}(({process_dir}[^<]*)\\+)?({process_name}[^<]+?))</Data>'] |
| edit_regex_field | process_guid |  | ['(?i)<Data Name\\*=(\'|")SourceProcessGuid(\'|")>\{({process_guid}[A-F0-9a-f-]+)\}</Data>'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")SourceProcessId(\'|")>({process_id}\d+)</Data>'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")TargetImage(\'|")>({process_path}(({process_dir}[^<]*)\\+)?({process_name}[^<]+?))</Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")TargetImage(\'|")>({process_path}(({process_dir}[^<]*)\\+)?({process_name}[^<]+?))</Data>'] |
| edit_regex_field | result |  | ['<Data Name\\*=(\'|")GrantedAccess(\'|")>({result}[^<]+)</Data>'] |
| edit_regex_field | time |  | ['<Data Name\\*=(\'|")UtcTime(\'|")>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)</Data>', '<TimeCreated SystemTime\\*=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")User(\'|")>(({domain}[^\\<]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")/>'] |