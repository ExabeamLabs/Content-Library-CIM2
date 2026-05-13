# Code Changes for microsoft-sysmon-xml-process-close-5-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'event_code', 'event_id', 'event_name', 'host', 'log_name', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |