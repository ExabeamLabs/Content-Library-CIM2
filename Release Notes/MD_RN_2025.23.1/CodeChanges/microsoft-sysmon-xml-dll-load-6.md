# Code Changes for microsoft-sysmon-xml-dll-load-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'event_id', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'host', 'log_name', 'operation', 'result', 'run_level', 'thread_id', 'time', 'user_sid'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}Driver loaded))'] |
| added_regex_field | operation |  | ['({operation}({event_name}Driver loaded))'] |
| removed_attribute | DupFields |  | N/A |