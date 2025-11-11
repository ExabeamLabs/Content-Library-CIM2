# Code Changes for microsoft-evsecurity-kv-audit-policy-modify-success-612 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'policy_name', 'user'] |
| edit_regex_field | host |  | ['ComputerName=({dest_host}({host}[\w.\-]+))'] |
| added_regex_field | dest_host |  | ['ComputerName=({dest_host}({host}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |