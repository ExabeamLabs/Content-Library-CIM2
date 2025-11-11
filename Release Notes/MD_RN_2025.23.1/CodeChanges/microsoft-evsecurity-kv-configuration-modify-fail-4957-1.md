# Code Changes for microsoft-evsecurity-kv-configuration-modify-fail-4957-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'event_name', 'failure_reason', 'host', 'operation_type', 'result', 'time'] |
| edit_regex_field | host |  | ['ComputerName=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['ComputerName=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |