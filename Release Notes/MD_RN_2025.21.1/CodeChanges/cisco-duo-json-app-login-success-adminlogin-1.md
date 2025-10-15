# Code Changes for cisco-duo-json-app-login-success-adminlogin-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_method', 'event_name', 'factor', 'first_name', 'full_name', 'host', 'last_name', 'object', 'operation', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | operation |  | ['({event_name}({operation}admin_login))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}admin_login))'] |
| removed_attribute | DupFields |  | N/A |