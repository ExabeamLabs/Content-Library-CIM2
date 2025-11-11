# Code Changes for hp-arubacpm-cef-radius-traffic-success-authsource (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_method', 'auth_server', 'dest_ip', 'dest_port', 'domain', 'email_address', 'event_name', 'host', 'network', 'result', 'src_mac', 'time', 'user', 'user_type'] |
| added_regex_field | auth_server |  | ['"host":"({auth_server}[^"]+)"'] |
| removed_attribute | DupFields |  | N/A |