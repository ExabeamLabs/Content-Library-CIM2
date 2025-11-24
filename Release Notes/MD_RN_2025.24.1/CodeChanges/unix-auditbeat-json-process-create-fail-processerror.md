# Code Changes for unix-auditbeat-json-process-create-fail-processerror (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_name', 'failure_reason', 'host', 'parent_process_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'time', 'user', 'user_id'] |
| edit_regex_field | host |  | ['"host":.+?name":"({dest_host}({host}[\w\-.]+?))(@[^"]*)?"'] |
| added_regex_field | dest_host |  | ['"host":.+?name":"({dest_host}({host}[\w\-.]+?))(@[^"]*)?"'] |
| removed_attribute | DupFields |  | N/A |