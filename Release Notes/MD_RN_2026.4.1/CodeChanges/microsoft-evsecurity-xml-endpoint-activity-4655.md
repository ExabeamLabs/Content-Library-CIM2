# Code Changes for microsoft-evsecurity-xml-endpoint-activity-4655 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_ip', 'dest_port', 'event_code', 'host', 'process_id', 'result', 'run_level', 'src_ip', 'src_port', 'task_name', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |