# Code Changes for microsoft-evsecurity-cef-endpoint-login-success-4624 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'host', 'key_length', 'location', 'login_id', 'login_type', 'process_name', 'process_path', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['\sdvchost=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['\sdvchost=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |