# Code Changes for microsoft-sysmon-xml-alert-trigger-success-25 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'channel', 'dest_host', 'event_code', 'host', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'run_level', 'thread_id', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |