# Code Changes for microsoft-evdnsserver-xml-network-notification-6001 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_guid |  | ['Guid\\*=(\'|")\{({process_guid}[^}\']+?)\}\''] |
| edit_regex_field | process_id |  | ['ProcessID\\*=(\'|")({process_id}\d+)'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\'"]+)'] |