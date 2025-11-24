# Code Changes for unix-unix-str-group-member-add-success-usermod (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_host', 'group_name', 'host', 'process_id', 'process_name', 'time'] |
| edit_regex_field | host |  | ['(T|\s)\d\d:\d\d:\d\d(\.?\S+)? ({dest_host}({host}[\w.\-]+))(\s\S+)?\susermod\[', '({time}\w+\s\d+\s\d\d:\d\d:\d\d)? ({dest_host}({host}[\w.\-]+))\s*usermod'] |
| edit_regex_field | time |  | ['({time}\w+\s\d+\s\d\d:\d\d:\d\d)? ({dest_host}({host}[\w.\-]+))\s*usermod', '\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-][^\s]+)'] |
| added_regex_field | dest_host |  | ['(T|\s)\d\d:\d\d:\d\d(\.?\S+)? ({dest_host}({host}[\w.\-]+))(\s\S+)?\susermod\[', '({time}\w+\s\d+\s\d\d:\d\d:\d\d)? ({dest_host}({host}[\w.\-]+))\s*usermod'] |
| removed_attribute | DupFields |  | N/A |