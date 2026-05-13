# Code Changes for microsoft-evsecurity-xml-network-listen-5154 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'host', 'process_dir', 'process_id', 'process_name', 'process_path', 'protocol', 'run_level', 'src_ip', 'src_port', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |