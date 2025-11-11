# Code Changes for microsoft-evsecurity-str-process-create-success-592 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'parent_process_guid', 'path', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'src_host', 'time', 'user'] |
| edit_regex_field | process_guid |  | ['New Process ID:\s+({process_id}({process_guid}[^\s]+))\s'] |
| added_regex_field | process_id |  | ['New Process ID:\s+({process_id}({process_guid}[^\s]+))\s'] |
| removed_attribute | DupFields |  | N/A |