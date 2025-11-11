# Code Changes for microsoft-evsecurity-kv-endpoint-unlock-success-4801-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | host |  | ['ComputerName=({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['ComputerName=({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |