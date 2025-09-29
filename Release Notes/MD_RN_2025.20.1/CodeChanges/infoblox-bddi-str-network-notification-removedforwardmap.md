# Code Changes for infoblox-bddi-str-network-notification-removedforwardmap (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_ip', 'dest_port', 'host', 'operation', 'process_id', 'process_name', 'src_host', 'src_ip', 'src_port'] |
| added_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |