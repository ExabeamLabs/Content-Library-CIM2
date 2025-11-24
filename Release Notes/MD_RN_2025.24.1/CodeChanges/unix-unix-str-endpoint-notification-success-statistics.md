# Code Changes for unix-unix-str-endpoint-notification-success-statistics (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes_in', 'bytes_out', 'dest_host', 'event_name', 'host', 'src_ip', 'time'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d ({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d ({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |