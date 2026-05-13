# Code Changes for microsoft-sysmon-xml-network-session-success-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'host', 'operation', 'path', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'protocol', 'run_level', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |