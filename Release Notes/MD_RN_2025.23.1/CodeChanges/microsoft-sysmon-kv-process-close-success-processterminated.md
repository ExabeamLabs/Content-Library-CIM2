# Code Changes for microsoft-sysmon-kv-process-close-success-processterminated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'host', 'operation_type', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({dest_host}({host}[\w\-.]+))\s)?', 'Hostname":"({dest_host}({host}[^"]+?))"', '\sComputer(?:Name)?\s*=\s*"?({dest_host}({host}[^\s"]+))'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({dest_host}({host}[\w\-.]+))\s)?', 'UtcTime:\s*({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)'] |
| added_regex_field | dest_host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({dest_host}({host}[\w\-.]+))\s)?', 'Hostname":"({dest_host}({host}[^"]+?))"', '\sComputer(?:Name)?\s*=\s*"?({dest_host}({host}[^\s"]+))'] |
| removed_attribute | DupFields |  | N/A |