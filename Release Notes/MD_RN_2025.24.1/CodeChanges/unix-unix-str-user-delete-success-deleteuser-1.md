# Code Changes for unix-unix-str-user-delete-success-deleteuser-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_host', 'dest_user', 'group_name', 'host', 'process_id', 'process_name'] |
| edit_regex_field | dest_user |  | ["delete\s+\'({account_name}({dest_user}[^']+))\'"] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d(\.\S+)? ({dest_host}({host}[\w.\-]+))\suserdel'] |
| added_regex_field | account_name |  | ["delete\s+\'({account_name}({dest_user}[^']+))\'"] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d(\.\S+)? ({dest_host}({host}[\w.\-]+))\suserdel'] |
| removed_attribute | DupFields |  | N/A |