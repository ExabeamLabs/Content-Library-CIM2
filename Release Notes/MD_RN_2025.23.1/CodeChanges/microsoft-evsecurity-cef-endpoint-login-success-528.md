# Code Changes for microsoft-evsecurity-cef-endpoint-login-success-528 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'auth_process', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['\sdvchost=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['\sdvchost=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |