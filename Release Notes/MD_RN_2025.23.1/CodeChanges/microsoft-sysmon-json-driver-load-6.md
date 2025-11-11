# Code Changes for microsoft-sysmon-json-driver-load-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'host', 'operation', 'result', 'time', 'user', 'user_sid'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}Driver loaded))'] |
| edit_regex_field | host |  | ['"Hostname":"({dest_host}({host}[^"]+))'] |
| added_regex_field | dest_host |  | ['"Hostname":"({dest_host}({host}[^"]+))'] |
| added_regex_field | operation |  | ['({operation}({event_name}Driver loaded))'] |
| removed_attribute | DupFields |  | N/A |