# Code Changes for microsoft-evsecurity-xml-network-session-success-5158-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'event_name', 'host', 'layer_name', 'ms_protocol_num', 'process_dir', 'process_id', 'process_name', 'process_path', 'run_level', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | ['"Computer":"({src_host}({host}[\w\-.]+))'] |
| added_regex_field | src_host |  | ['"Computer":"({src_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |