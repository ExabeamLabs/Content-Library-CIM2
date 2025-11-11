# Code Changes for microsoft-windows-kv-dhcp-session-success-assign (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'time', 'user'] |
| edit_regex_field | dest_host |  | ['Host Name=({dest_host}[\w\-.]+))'] |
| added_regex_field | user |  | ['Host Name=({user}[\w\.\-]{1,40}\$?)'] |
| removed_attribute | DupFields |  | N/A |