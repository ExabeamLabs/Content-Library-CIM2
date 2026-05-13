# Code Changes for microsoft-evsecurity-xml-network-traffic-fail-5152 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'dest_ip', 'dest_port', 'direction', 'event_code', 'event_name', 'failure_reason', 'host', 'process_dir', 'process_id', 'process_name', 'process_path', 'protocol', 'result', 'run_level', 'src_ip', 'src_port', 'task_name', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |