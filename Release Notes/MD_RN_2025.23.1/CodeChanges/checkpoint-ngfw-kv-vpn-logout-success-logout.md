# Code Changes for checkpoint-ngfw-kv-vpn-logout-success-logout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'domain', 'email_address', 'event_name', 'failure_reason', 'first_name', 'host', 'last_name', 'session_duration', 'src_ip', 'src_port', 'time', 'user', 'user_ou'] |
| added_regex_field | event_name |  | ['\Waction:"({event_name}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |