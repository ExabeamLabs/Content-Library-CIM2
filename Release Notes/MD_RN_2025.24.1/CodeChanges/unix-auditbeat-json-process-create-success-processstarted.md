# Code Changes for unix-auditbeat-json-process-create-success-processstarted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'event_name', 'hash_md5', 'host', 'parent_process_id', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'time', 'user', 'user_id'] |
| edit_regex_field | host |  | ['"hostname":"({dest_host}({host}[\w\-.]+?))(@[^"]*)?"'] |
| added_regex_field | dest_host |  | ['"hostname":"({dest_host}({host}[\w\-.]+?))(@[^"]*)?"'] |
| removed_attribute | DupFields |  | N/A |