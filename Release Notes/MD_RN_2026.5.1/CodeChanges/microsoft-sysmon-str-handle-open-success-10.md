# Code Changes for microsoft-sysmon-str-handle-open-success-10 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_process_dir', 'dest_process_id', 'dest_process_name', 'dest_process_path', 'event_code', 'event_id', 'host', 'operation', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'provider_name', 'result', 'thread_id', 'time', 'user'] |
| added_regex_field | channel |  | ['channel="({channel}[^"]+)'] |