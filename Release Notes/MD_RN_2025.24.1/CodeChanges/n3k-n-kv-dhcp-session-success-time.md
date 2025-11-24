# Code Changes for n3k-n-kv-dhcp-session-success-time (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_port', 'src_mac', 'time', 'user'] |
| edit_regex_field | dest_host |  | ['("|\s)Host(":\s+|=)"?({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | user |  | ['("|\s)Host(":\s+|=)"?({dest_host}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |