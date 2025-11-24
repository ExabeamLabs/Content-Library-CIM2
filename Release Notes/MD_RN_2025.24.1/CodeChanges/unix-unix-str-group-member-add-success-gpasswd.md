# Code Changes for unix-unix-str-group-member-add-success-gpasswd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_host', 'group_name', 'host', 'process_id', 'process_name', 'user'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d ({dest_host}({host}[\w.\-]+))\sgpasswd'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d ({dest_host}({host}[\w.\-]+))\sgpasswd'] |
| removed_attribute | DupFields |  | N/A |