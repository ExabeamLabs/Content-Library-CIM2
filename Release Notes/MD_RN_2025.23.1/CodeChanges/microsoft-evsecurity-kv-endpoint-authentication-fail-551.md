# Code Changes for microsoft-evsecurity-kv-endpoint-authentication-fail-551 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'failure_code', 'failure_reason', 'host', 'log_name', 'result', 'service_name', 'session_id', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['({src_host}({host}[\w\-\.]+))\s+None'] |
| added_regex_field | src_host |  | ['({src_host}({host}[\w\-\.]+))\s+None'] |
| removed_attribute | DupFields |  | N/A |