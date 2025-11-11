# Code Changes for cef-defender-atp-2 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_host', 'dest_ip', 'dest_port', 'event_name', 'operation', 'process_dir', 'process_integrity', 'process_name', 'process_path', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | category |  | ['category"+:\s*"+({event_name}({category}[^"]+))'] |
| added_regex_field | event_name |  | ['category"+:\s*"+({event_name}({category}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |