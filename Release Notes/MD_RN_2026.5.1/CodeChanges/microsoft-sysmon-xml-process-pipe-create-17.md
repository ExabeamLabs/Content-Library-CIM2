# Code Changes for microsoft-sysmon-xml-process-pipe-create-17 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_name', 'host', 'log_name', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'run_level', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |