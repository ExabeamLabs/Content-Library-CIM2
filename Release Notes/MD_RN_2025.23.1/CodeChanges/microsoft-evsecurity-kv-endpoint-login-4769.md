# Code Changes for microsoft-evsecurity-kv-endpoint-login-4769 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'failure_code', 'host', 'result_code', 'service_name', 'src_host', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user'] |
| edit_regex_field | result_code |  | ['Failure Code:\s*({failure_code}({result_code}.+?))[\s;]*Transited Services'] |
| added_regex_field | failure_code |  | ['Failure Code:\s*({failure_code}({result_code}.+?))[\s;]*Transited Services'] |
| removed_attribute | DupFields |  | N/A |