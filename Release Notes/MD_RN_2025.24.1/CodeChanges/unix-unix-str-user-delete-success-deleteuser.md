# Code Changes for unix-unix-str-user-delete-success-deleteuser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_host', 'dest_user', 'host', 'process_id', 'process_name', 'time'] |
| edit_regex_field | dest_user |  | ["delete user \'({account_name}({dest_user}[^']+))\'"] |
| edit_regex_field | host |  | ['(\s|T)\d\d:\d\d:\d\d(\.?\S+)? ({dest_host}({host}[\w.\-]+))\suserdel', '({time}\w+\s\d+\s\d\d:\d\d:\d\d)? ({dest_host}({host}[\w.\-]+))\suserdel'] |
| edit_regex_field | time |  | ['({time}\w+\s\d+\s\d\d:\d\d:\d\d)? ({dest_host}({host}[\w.\-]+))\suserdel', '\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-][^\s]+)'] |
| added_regex_field | account_name |  | ["delete user \'({account_name}({dest_user}[^']+))\'"] |
| added_regex_field | dest_host |  | ['(\s|T)\d\d:\d\d:\d\d(\.?\S+)? ({dest_host}({host}[\w.\-]+))\suserdel', '({time}\w+\s\d+\s\d\d:\d\d:\d\d)? ({dest_host}({host}[\w.\-]+))\suserdel'] |
| removed_attribute | DupFields |  | N/A |