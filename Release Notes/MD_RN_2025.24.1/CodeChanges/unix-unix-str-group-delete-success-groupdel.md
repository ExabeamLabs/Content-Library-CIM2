# Code Changes for unix-unix-str-group-delete-success-groupdel (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'group_name', 'host', 'process_id', 'process_name'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d(\.\S+)? ({dest_host}({host}[\w.\-]+))\sgroupdel'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d(\.\S+)? ({dest_host}({host}[\w.\-]+))\sgroupdel'] |
| removed_attribute | DupFields |  | N/A |