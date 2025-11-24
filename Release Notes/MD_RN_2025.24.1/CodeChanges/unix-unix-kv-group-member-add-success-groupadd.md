# Code Changes for unix-unix-kv-group-member-add-success-groupadd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_group', 'dest_host', 'host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | ['<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({dest_host}({host}[\w.\-]+)) groupadd'] |
| edit_regex_field | time |  | ['<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({dest_host}({host}[\w.\-]+)) groupadd'] |
| added_regex_field | dest_host |  | ['<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({dest_host}({host}[\w.\-]+)) groupadd'] |
| removed_attribute | DupFields |  | N/A |