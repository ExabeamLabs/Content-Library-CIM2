# Code Changes for microsoft-evsecurity-kv-user-delete-success-630 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | dest_domain |  | ['Target Account Name:\s+(?=\w)({account_name}({dest_user}.+?))\s+Target Domain:\s+(?=\w)({dest_domain}.+?)\s+Target Account ID:\s\%\{({dest_user_sid}[^}]+)\}'] |
| edit_regex_field | dest_user |  | ['Target Account Name:\s+(?=\w)({account_name}({dest_user}.+?))\s+Target Domain:\s+(?=\w)({dest_domain}.+?)\s+Target Account ID:\s\%\{({dest_user_sid}[^}]+)\}'] |
| edit_regex_field | dest_user_sid |  | ['Target Account Name:\s+(?=\w)({account_name}({dest_user}.+?))\s+Target Domain:\s+(?=\w)({dest_domain}.+?)\s+Target Account ID:\s\%\{({dest_user_sid}[^}]+)\}'] |
| edit_regex_field | host |  | ['(?i)(((audit|success)( |_)(success|audit))|information)(\s+|,)({host}({dest_host}[\w.\-]+))', '({host}({dest_host}[^\/\s]+))\/Security \(630\)', 'Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}({dest_host}[\w\-.]+?))(\"|\s)'] |
| added_regex_field | account_name |  | ['Target Account Name:\s+(?=\w)({account_name}({dest_user}.+?))\s+Target Domain:\s+(?=\w)({dest_domain}.+?)\s+Target Account ID:\s\%\{({dest_user_sid}[^}]+)\}'] |
| added_regex_field | dest_host |  | ['(?i)(((audit|success)( |_)(success|audit))|information)(\s+|,)({host}({dest_host}[\w.\-]+))', '({host}({dest_host}[^\/\s]+))\/Security \(630\)', 'Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}({dest_host}[\w\-.]+?))(\"|\s)'] |
| removed_attribute | DupFields |  | N/A |