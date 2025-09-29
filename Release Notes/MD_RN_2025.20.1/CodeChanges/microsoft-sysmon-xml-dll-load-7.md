# Code Changes for microsoft-sysmon-xml-dll-load-7 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'host', 'log_name', 'operation', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'service_state', 'signature', 'signed', 'task_name', 'thread_id', 'time', 'user_sid'] |
| removed_regex_field | state |  | [] |
| added_regex_field | service_state |  | ['<Data Name\\*=(\'|")State(\'|")>({service_state}[^<]+)<'] |