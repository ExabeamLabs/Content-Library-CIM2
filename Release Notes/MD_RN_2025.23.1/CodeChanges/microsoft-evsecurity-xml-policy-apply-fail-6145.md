# Code Changes for microsoft-evsecurity-xml-policy-apply-fail-6145 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'error_code', 'event_code', 'event_id', 'event_name', 'failure_code', 'host', 'policy_name', 'process_id', 'run_level', 'severity', 'thread_id', 'time'] |
| edit_regex_field | error_code |  | ['<Data Name\\*=(\'|")ErrorCode(\'|")>({failure_code}({error_code}\d+))<\/Data>'] |
| added_regex_field | failure_code |  | ['<Data Name\\*=(\'|")ErrorCode(\'|")>({failure_code}({error_code}\d+))<\/Data>'] |
| removed_attribute | DupFields |  | N/A |