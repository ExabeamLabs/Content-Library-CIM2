# Code Changes for unix-unix-str-group-member-add-success-usermod-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_host', 'group_name', 'host', 'process_id', 'process_name', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | ['<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({dest_host}({host}[\w.\-]+)) usermod'] |
| edit_regex_field | time |  | ['<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({dest_host}({host}[\w.\-]+)) usermod'] |
| added_regex_field | dest_host |  | ['<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({dest_host}({host}[\w.\-]+)) usermod'] |
| removed_attribute | DupFields |  | N/A |