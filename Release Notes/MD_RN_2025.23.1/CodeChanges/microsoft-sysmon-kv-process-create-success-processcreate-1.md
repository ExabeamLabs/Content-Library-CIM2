# Code Changes for microsoft-sysmon-kv-process-create-success-processcreate-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_name', 'hash_md5', 'host', 'login_id', 'parent_process_dir', 'parent_process_guid', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_integrity', 'process_name', 'process_path', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}[\w\-.]+)\s', '\sComputer="({src_host}({host}[\w\-.]+))"'] |
| added_regex_field | src_host |  | ['\sComputer="({src_host}({host}[\w\-.]+))"'] |
| removed_attribute | DupFields |  | N/A |