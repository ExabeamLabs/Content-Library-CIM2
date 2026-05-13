# Code Changes for microsoft-evsecurity-xml-network-session-fail-4984 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'channel', 'dest_ip', 'dest_port', 'event_code', 'failure_reason', 'host', 'process_id', 'role', 'run_level', 'service_state', 'src_ip', 'src_port', 'task_name', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |