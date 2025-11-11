# Code Changes for microsoft-sysmon-kv-file-write-success-filecreate (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'operation_type', 'parent_process_guid', 'path', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({dest_host}({host}[\w\-.]+))\s)?', 'Hostname":"({dest_host}({host}[\w\-.]+?))"', '\sComputer(?:Name)?\s*=\s*"?({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | process_dir |  | ['"Image":"({path}({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+)))"', '\s+Image:\s*({path}({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?)))\s+TargetFilename:'] |
| edit_regex_field | process_name |  | ['"Image":"({path}({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+)))"', '\s+Image:\s*({path}({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?)))\s+TargetFilename:'] |
| edit_regex_field | process_path |  | ['"Image":"({path}({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+)))"', '\s+Image:\s*({path}({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?)))\s+TargetFilename:'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({dest_host}({host}[\w\-.]+))\s)?', 'UtcTime:\s*({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)'] |
| added_regex_field | dest_host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({dest_host}({host}[\w\-.]+))\s)?', 'Hostname":"({dest_host}({host}[\w\-.]+?))"', '\sComputer(?:Name)?\s*=\s*"?({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | path |  | ['"Image":"({path}({process_path}(({process_dir}[^"]*?)[\\\/]+)?({process_name}[^"\\\/]+)))"', '\s+Image:\s*({path}({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?)))\s+TargetFilename:'] |
| removed_attribute | DupFields |  | N/A |