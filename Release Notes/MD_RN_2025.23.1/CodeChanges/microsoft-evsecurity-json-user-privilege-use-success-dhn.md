# Code Changes for microsoft-evsecurity-json-user-privilege-use-success-dhn (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'event_name', 'full_name', 'host', 'login_id', 'object', 'object_server', 'object_type', 'privileges', 'process_dir', 'process_name', 'process_path', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['\"dhn\":\"({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['\"dhn\":\"({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |