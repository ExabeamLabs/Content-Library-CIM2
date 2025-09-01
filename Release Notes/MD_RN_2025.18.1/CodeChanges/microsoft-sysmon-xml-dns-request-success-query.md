# Code Changes for microsoft-sysmon-xml-dns-request-success-query (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dns_query |  | ['<Data Name\\*=(\'|")QueryName(\'|")>({dns_query}.+?)\s*</Data>'] |
| edit_regex_field | dns_response |  | ['<Data Name\\*=(\'|")QueryResults(\'|")>({dns_response}.+?)\s*</Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")Image(\'|")>(<|&lt;)({process_path}(({process_dir}[^<]*)\\+)?({process_name}.+?))(<|&gt;)<\/Data>', '<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<]*)\\+)?({process_name}.+?))</Data>'] |
| edit_regex_field | process_guid |  | ['(?i)<Data Name\\*=(\'|")ProcessGuid(\'|")>\{({process_guid}[A-F0-9a-f-]+)\}</Data>'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")ProcessId(\'|")>({process_id}\d+)</Data>'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")Image(\'|")>(<|&lt;)({process_path}(({process_dir}[^<]*)\\+)?({process_name}.+?))(<|&gt;)<\/Data>', '<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<]*)\\+)?({process_name}.+?))</Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")Image(\'|")>(<|&lt;)({process_path}(({process_dir}[^<]*)\\+)?({process_name}.+?))(<|&gt;)<\/Data>', '<Data Name\\*=(\'|")Image(\'|")>({process_path}(({process_dir}[^<]*)\\+)?({process_name}.+?))</Data>'] |
| edit_regex_field | time |  | ['<Data Name\\*=(\'|")UtcTime(\'|")>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)</Data>', '<TimeCreated SystemTime\\*=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}.+?)(\'|")/>'] |