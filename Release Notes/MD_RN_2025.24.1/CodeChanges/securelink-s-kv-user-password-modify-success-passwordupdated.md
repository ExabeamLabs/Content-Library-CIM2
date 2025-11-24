# Code Changes for securelink-s-kv-user-password-modify-success-passwordupdated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'email_address', 'email_domain', 'event_category', 'event_name', 'host', 'result_reason', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | result_reason |  | ['Text:\s*(\[[^\]]+\]\s+)?({result_reason}[^",]+)'] |
| removed_attribute | DupFields |  | N/A |