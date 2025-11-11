# Code Changes for secureauth-idp-kv-user-password-modify-fail-41070 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'category', 'dest_host', 'email_address', 'event_code', 'failure_reason', 'host', 'priority', 'realm', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| added_regex_field | failure_reason |  | ['\WEventID="[^\]]*?\]\s({failure_reason}[^"]+)\s*"'] |
| removed_attribute | DupFields |  | N/A |