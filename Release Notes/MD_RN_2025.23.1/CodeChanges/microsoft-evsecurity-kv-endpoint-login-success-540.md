# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-540 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['(?i)(((audit|success)( |_)(success|audit))|information)\s*,?\s*({dest_host}({host}[\w\-.]+))', '({dest_host}({host}[^\/\s]+))\/Security\s+\(', 'Computer(\w+)?["\s]*(:|=)\s*"?({dest_host}({host}[\w\-.]+?))("|\s)'] |
| added_regex_field | dest_host |  | ['(?i)(((audit|success)( |_)(success|audit))|information)\s*,?\s*({dest_host}({host}[\w\-.]+))', '({dest_host}({host}[^\/\s]+))\/Security\s+\(', 'Computer(\w+)?["\s]*(:|=)\s*"?({dest_host}({host}[\w\-.]+?))("|\s)'] |
| removed_attribute | DupFields |  | N/A |