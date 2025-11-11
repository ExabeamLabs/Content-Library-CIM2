# Code Changes for microsoft-evsecurity-kv-process-create-success-592 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'login_id', 'parent_process_guid', 'path', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | process_guid |  | ['New\s*Process\s*ID:\s*(?:-|({process_id}({process_guid}\d+)))\s'] |
| added_regex_field | process_id |  | ['New\s*Process\s*ID:\s*(?:-|({process_id}({process_guid}\d+)))\s'] |
| removed_attribute | DupFields |  | N/A |