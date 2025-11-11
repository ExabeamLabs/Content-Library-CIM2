# Code Changes for microsoft-evsecurity-kv-network-session-success-5156-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'direction', 'event_code', 'host', 'layer_name', 'process_dir', 'process_id', 'process_name', 'process_path', 'protocol', 'src_ip', 'src_port', 'time'] |
| removed_regex_field | ms_protocol_num |  | [] |
| added_regex_field | protocol |  | ['通訊協定:\s*({protocol}\d+)'] |