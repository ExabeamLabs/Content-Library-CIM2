# Code Changes for microsoft-evsecurity-kv-network-session-success-5158 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'event_name', 'host', 'layer_name', 'process_dir', 'process_id', 'process_name', 'process_path', 'protocol', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | ['Computer=\s*({src_host}({host}[\w\-.]*))'] |
| removed_regex_field | ms_protocol_num |  | [] |
| added_regex_field | protocol |  | ['Protocol:\s*({protocol}\d+)'] |
| added_regex_field | src_host |  | ['Computer=\s*({src_host}({host}[\w\-.]*))'] |
| removed_attribute | DupFields |  | N/A |