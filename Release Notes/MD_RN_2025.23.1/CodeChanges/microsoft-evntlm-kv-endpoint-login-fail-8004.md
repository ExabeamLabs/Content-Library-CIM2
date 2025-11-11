# Code Changes for microsoft-evntlm-kv-endpoint-login-fail-8004 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'policy_name', 'resource', 'src_host', 'time', 'user'] |
| edit_regex_field | host |  | ['ComputerName=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['ComputerName=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |