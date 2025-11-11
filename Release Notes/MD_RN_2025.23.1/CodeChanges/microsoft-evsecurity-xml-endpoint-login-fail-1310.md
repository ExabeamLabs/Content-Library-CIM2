# Code Changes for microsoft-evsecurity-xml-endpoint-login-fail-1310 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'failure_code', 'failure_reason', 'host', 'provider_name', 'result', 'result_code', 'run_level', 'time', 'user'] |
| edit_regex_field | result_code |  | ['status=([^:]+:)({failure_code}({result_code}[^:]+)):'] |
| added_regex_field | failure_code |  | ['status=([^:]+:)({failure_code}({result_code}[^:]+)):'] |
| removed_attribute | DupFields |  | N/A |