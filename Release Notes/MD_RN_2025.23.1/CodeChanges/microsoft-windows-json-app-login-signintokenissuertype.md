# Code Changes for microsoft-windows-json-app-login-signintokenissuertype (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_method', 'category', 'country_code', 'email_address', 'email_domain', 'error_code', 'event_name', 'failure_reason', 'first_name', 'full_name', 'host', 'last_name', 'operation', 'result', 'severity', 'src_host', 'src_ip', 'src_port', 'time', 'user_agent', 'user_uid'] |
| edit_regex_field | operation |  | ['"operationName":\s"({event_name}({operation}[^"]+))"'] |
| added_regex_field | event_name |  | ['"operationName":\s"({event_name}({operation}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |