# Code Changes for unix-unix-str-endpoint-logout-success-sshsdisconnect (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'email_address', 'event_name', 'host', 'src_ip', 'time', 'user'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d ({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d ({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |