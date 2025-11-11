# Code Changes for pan-ngfw-cef-vpn-login-prelogin-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'auth_method', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'event_name', 'host', 'operation', 'os', 'result', 'src_country', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | event_name |  | ['PanOSEventID=({operation}({event_name}[^=]+?))\s\w+=', '\sName=({operation}({event_name}[^=]+?))\s\w+='] |
| added_regex_field | operation |  | ['PanOSEventID=({operation}({event_name}[^=]+?))\s\w+=', '\sName=({operation}({event_name}[^=]+?))\s\w+='] |