# Code Changes for forcepoint-ngfw-cef-app-activity-log (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'bytes_in', 'bytes_out', 'category', 'dest_host', 'dest_interface', 'dest_ip', 'dest_port', 'event_name', 'host', 'operation', 'protocol', 'src_interface', 'src_ip', 'src_mac', 'src_port', 'time'] |
| added_regex_field | event_name |  | ['CEF:\s*\d+\|([^\|]+\|){4}({event_name}[^\|]+)'] |
| removed_attribute | DupFields |  | N/A |