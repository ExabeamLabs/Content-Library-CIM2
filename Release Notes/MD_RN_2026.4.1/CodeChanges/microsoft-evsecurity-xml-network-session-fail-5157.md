# Code Changes for microsoft-evsecurity-xml-network-session-fail-5157 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'dest_ip', 'dest_port', 'direction', 'event_code', 'event_name', 'failure_reason', 'host', 'layer_name', 'operation_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'protocol', 'run_level', 'src_host', 'src_ip', 'src_port', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |