# Code Changes for secureauth-idp-kv-endpoint-authentication-fail-51140 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'browser', 'category', 'dest_host', 'email_address', 'event_code', 'failure_reason', 'host', 'os', 'priority', 'realm', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| added_regex_field | failure_reason |  | ['Message="\s*({failure_reason}[^"]+)\s*"', '\WEventID="[^\]]*?\]\s({failure_reason}[^"]+)\s*"*$'] |
| removed_attribute | DupFields |  | N/A |