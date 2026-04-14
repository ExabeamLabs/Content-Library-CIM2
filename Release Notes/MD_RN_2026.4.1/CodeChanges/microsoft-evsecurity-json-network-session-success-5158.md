# Code Changes for microsoft-evsecurity-json-network-session-success-5158 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_name', 'host', 'layer_name', 'ms_protocol_num', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_ip', 'src_port', 'time'] |
| added_regex_field | channel |  | ['"channel":"({channel}[^"]+)"'] |