# Code Changes for microsoft-evsecurity-json-endpoint-login-673 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'failure_code', 'host', 'result_code', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user'] |
| edit_regex_field | result_code |  | ['Failure Code:\s*({failure_code}({result_code}[\w\-]+))'] |
| added_regex_field | failure_code |  | ['Failure Code:\s*({failure_code}({result_code}[\w\-]+))'] |
| removed_attribute | DupFields |  | N/A |