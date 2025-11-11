# Code Changes for checkpoint-ngfw-kv-vpn-login-success-login (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_method', 'dest_ip', 'dest_port', 'domain', 'email_address', 'event_name', 'failure_reason', 'first_name', 'full_name', 'host', 'last_name', 'operation', 'origin_ip', 'origin_name', 'os', 'product_name', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | operation |  | ['action:"+({event_name}({operation}[^"]+))'] |
| added_regex_field | event_name |  | ['action:"+({event_name}({operation}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |