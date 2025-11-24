# Code Changes for unix-unix-kv-endpoint-login-success-auid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'host', 'login_type_text', 'operation_type', 'process_id', 'session_id', 'time', 'user_id'] |
| edit_regex_field | login_type_text |  | ['type=({operation_type}({login_type_text}[^\s]+))'] |
| added_regex_field | operation_type |  | ['type=({operation_type}({login_type_text}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |