# Code Changes for unix-unix-str-process-create-success-proccreate (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'file_name', 'file_path', 'host', 'operation', 'process_command_line', 'time', 'user'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-\.]+))\sassh:'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-\.]+))\sassh:'] |
| removed_attribute | DupFields |  | N/A |