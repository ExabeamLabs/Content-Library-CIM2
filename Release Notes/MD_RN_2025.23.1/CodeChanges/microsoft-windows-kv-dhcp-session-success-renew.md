# Code Changes for microsoft-windows-kv-dhcp-session-success-renew (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'host', 'time', 'user'] |
| added_regex_field | user |  | ['\sHost Name=({user}[\w\.\-]{1,40}\$?)'] |
| removed_attribute | DupFields |  | N/A |