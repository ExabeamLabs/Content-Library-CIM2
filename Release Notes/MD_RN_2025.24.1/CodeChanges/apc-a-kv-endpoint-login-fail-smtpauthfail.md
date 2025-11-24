# Code Changes for apc-a-kv-endpoint-login-fail-smtpauthfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_ip', 'dest_port', 'domain', 'email_address', 'event_name', 'failure_reason', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | event_name |  | ['classifier="({failure_reason}({event_name}[^"]+))"'] |
| added_regex_field | failure_reason |  | ['classifier="({failure_reason}({event_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |