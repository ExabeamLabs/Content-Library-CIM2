# Code Changes for microsoft-evsecurity-kv-process-create-success-26304688 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'path', 'process_dir', 'process_name', 'process_path', 'src_host', 'time', 'user'] |
| edit_regex_field | host |  | ['shost=({src_host}({host}[\w\-.]+))'] |
| added_regex_field | src_host |  | ['shost=({src_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |