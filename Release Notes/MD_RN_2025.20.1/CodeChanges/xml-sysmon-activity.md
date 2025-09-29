# Code Changes for xml-sysmon-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'log_name', 'operation', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'service_state', 'task_name', 'thread_id', 'time', 'user_sid'] |
| removed_regex_field | state |  | [] |
| added_regex_field | service_state |  | ['<Data Name\\*=(\'|")State(\'|")>({service_state}[^<]+)<'] |