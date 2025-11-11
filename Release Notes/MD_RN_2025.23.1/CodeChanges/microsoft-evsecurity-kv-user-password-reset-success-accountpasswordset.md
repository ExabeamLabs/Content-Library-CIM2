# Code Changes for microsoft-evsecurity-kv-user-password-reset-success-accountpasswordset (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | host |  | ['(?i)((audit|success|failure)( |_)(success|audit|failure))\s+({dest_host}({host}[\w\-.]+))\s+Account Management', '(?i)(information)(,|\s+)({dest_host}({host}[\w.\-]+))', '({dest_host}({host}[^\/\s]+))\/Security', 'ComputerName=({dest_host}({host}[\w.\-]+))'] |
| added_regex_field | dest_host |  | ['(?i)((audit|success|failure)( |_)(success|audit|failure))\s+({dest_host}({host}[\w\-.]+))\s+Account Management', '(?i)(information)(,|\s+)({dest_host}({host}[\w.\-]+))', '({dest_host}({host}[^\/\s]+))\/Security', 'ComputerName=({dest_host}({host}[\w.\-]+))'] |
| removed_attribute | DupFields |  | N/A |