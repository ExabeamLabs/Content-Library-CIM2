# Code Changes for microsoft-evsecurity-xml-policy-apply-fail-6145 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | error_code |  | ['<Data Name\\*=(\'|")ErrorCode(\'|")>({error_code}\d+)<\/Data>'] |
| edit_regex_field | policy_name |  | ['<Data Name\\*=(\'|")GPOList(\'|")>({policy_name}[^<]+)<'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")'] |