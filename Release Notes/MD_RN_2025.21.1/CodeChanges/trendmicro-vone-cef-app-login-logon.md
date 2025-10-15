# Code Changes for trendmicro-vone-cef-app-login-logon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'device_id', 'event_category', 'event_code', 'event_name', 'full_name', 'host', 'operation', 'result', 'role', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | event_name |  | [' cs3=({operation}({event_name}[^=]+?))((\s+\w+=)|\s*$)'] |
| added_regex_field | operation |  | [' cs3=({operation}({event_name}[^=]+?))((\s+\w+=)|\s*$)'] |
| removed_attribute | DupFields |  | N/A |