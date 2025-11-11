# Code Changes for fireeye-networksecurity-cef-alert-trigger-success-fireeye (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'category', 'dest_host', 'dest_ip', 'dest_port', 'email_address', 'event_name', 'host', 'malware_file_name', 'malware_url', 'object', 'operation', 'resource', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | operation |  | ['CEF:([^\|]*\|){4}({event_name}({operation}[^\|]+))'] |
| edit_regex_field | resource |  | ['request=({object}({resource}[^\s=]+))\s*(\w+=|$)'] |
| added_regex_field | event_name |  | ['CEF:([^\|]*\|){4}({event_name}({operation}[^\|]+))'] |
| added_regex_field | object |  | ['request=({object}({resource}[^\s=]+))\s*(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |