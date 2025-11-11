# Code Changes for microsoft-windows-cef-dhcp-session-success-dhcpserver (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'host', 'time', 'user'] |
| added_regex_field | user |  | ['\sdhost=({user}[\w\.\-]{1,40}\$?)'] |
| removed_attribute | DupFields |  | N/A |