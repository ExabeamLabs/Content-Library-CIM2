# Code Changes for rubrik-cdm-kv-app-login-success-loggedin-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_severity', 'auth_method', 'dest_host', 'email_address', 'event_code', 'event_name', 'host', 'object', 'object_id', 'object_type', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['nodeId="({dest_host}({host}[^"]+))"'] |
| added_regex_field | dest_host |  | ['nodeId="({dest_host}({host}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |