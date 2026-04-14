# Code Changes for microsoft-evsecurity-json-network-session-success-5156-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_ip', 'dest_port', 'direction', 'event_code', 'event_name', 'host', 'layer_name', 'ms_protocol_num', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_ip', 'src_port', 'time'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |