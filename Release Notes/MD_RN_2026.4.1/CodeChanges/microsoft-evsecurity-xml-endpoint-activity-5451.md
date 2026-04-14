# Code Changes for microsoft-evsecurity-xml-endpoint-activity-5451 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_ip', 'dest_port', 'dest_translated_ip', 'duration', 'event_code', 'host', 'process_id', 'result', 'role', 'run_level', 'src_ip', 'src_port', 'src_translated_ip', 'task_name', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |