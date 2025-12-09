# Code Changes for crowdstrike-falcon-cef-app-login-success-startevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'cid', 'dest_host', 'email_address', 'email_domain', 'event_name', 'host', 'operation', 'operation_details', 'result', 'session_id', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}RemoteResponseSessionStartEvent))'] |
| edit_regex_field | host |  | ['"HostnameField":\s*"({dest_host}({host}[^"@]+))"'] |
| added_regex_field | dest_host |  | ['"HostnameField":\s*"({dest_host}({host}[^"@]+))"'] |
| added_regex_field | operation |  | ['({operation}({event_name}RemoteResponseSessionStartEvent))'] |
| removed_attribute | DupFields |  | N/A |