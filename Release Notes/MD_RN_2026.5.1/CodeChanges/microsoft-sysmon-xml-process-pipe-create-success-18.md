# Code Changes for microsoft-sysmon-xml-process-pipe-create-success-18 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'host', 'log_name', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'run_level', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |