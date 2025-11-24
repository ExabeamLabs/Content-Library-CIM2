# Code Changes for unix-unix-kv-endpoint-activity-fail-shellcmdmatchfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'event_name', 'host', 'src_ip', 'time', 'user'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d ({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d(\.\S+)? \d\d\d\d ({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |