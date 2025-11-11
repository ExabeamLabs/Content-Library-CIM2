# Code Changes for microsoft-evsecurity-kv-user-privilege-use-success-4674-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object_name', 'object_server', 'object_type', 'privileges', 'process_dir', 'process_name', 'process_path', 'result', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['Computer(\w+)?["\s]*(:|=)\s*"?({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['Computer(\w+)?["\s]*(:|=)\s*"?({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |