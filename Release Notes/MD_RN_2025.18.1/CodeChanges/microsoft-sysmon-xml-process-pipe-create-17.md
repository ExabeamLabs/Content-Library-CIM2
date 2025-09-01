# Code Changes for microsoft-sysmon-xml-process-pipe-create-17 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_name |  | ['<Data Name\\*=(\'|")EventType(\'|")>({event_name}[^<]+)<\/Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?)?)<\/Data>'] |
| edit_regex_field | process_guid |  | ['<Data Name\\*=(\'|")ProcessGuid(\'|")>({process_guid}[^<]+)<\/Data>'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")ProcessId(\'|")>({process_id}\d+)<\/Data>'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?)?)<\/Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?)?)<\/Data>'] |
| edit_regex_field | time |  | ['<Data Name\\*=(\'|")UtcTime(\'|")>({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d+)<\/Data>'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")'] |