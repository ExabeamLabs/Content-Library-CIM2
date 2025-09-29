# Code Changes for unix-unix-kv-service-stop-success-servicestop (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'account_name', 'additional_info', 'event_name', 'host', 'host_ip', 'operation', 'operation_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'session_id', 'src_port', 'time', 'user_uid'] |
| removed_regex_field | audispd_type |  | [] |
| edit_regex_field | operation_type |  | ['type=(?:({event_name}USER_\S+)|({operation_type}\S+))'] |
| added_regex_field | event_name |  | ['type=(?:({event_name}USER_\S+)|({operation_type}\S+))'] |