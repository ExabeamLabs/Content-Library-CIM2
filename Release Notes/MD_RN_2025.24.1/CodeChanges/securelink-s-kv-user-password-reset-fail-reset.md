# Code Changes for securelink-s-kv-user-password-reset-fail-reset (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'email_address', 'email_domain', 'event_category', 'event_name', 'failure_reason', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | failure_reason |  | ['Text:\s*(\[[^\]]+\]\s+)?({failure_reason}[^",]+)'] |
| removed_attribute | DupFields |  | N/A |