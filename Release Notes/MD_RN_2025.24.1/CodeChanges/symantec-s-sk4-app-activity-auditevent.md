# Code Changes for symantec-s-sk4-app-activity-auditevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'dest_host', 'event_name', 'event_subtype', 'host', 'operation', 'src_host', 'time', 'user'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w.\-]+))\s+SymantecServer:\s*({src_host}[^,]+)(,|\s*$)'] |
| edit_regex_field | src_host |  | ['({dest_host}({host}[\w.\-]+))\s+SymantecServer:\s*({src_host}[^,]+)(,|\s*$)'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w.\-]+))\s+SymantecServer:\s*({src_host}[^,]+)(,|\s*$)'] |
| removed_attribute | DupFields |  | N/A |