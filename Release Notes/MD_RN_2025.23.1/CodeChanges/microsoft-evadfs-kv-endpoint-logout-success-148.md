# Code Changes for microsoft-evadfs-kv-endpoint-logout-success-148 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'channel', 'dest_host', 'event_code', 'host', 'operation', 'time'] |
| edit_regex_field | host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))'] |
| added_regex_field | dest_host |  | ['ComputerName(:|=)\s*({dest_host}({host}[\w.-]+))'] |
| removed_attribute | DupFields |  | N/A |