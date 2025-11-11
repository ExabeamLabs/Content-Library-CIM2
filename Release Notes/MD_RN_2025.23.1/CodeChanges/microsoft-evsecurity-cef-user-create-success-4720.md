# Code Changes for microsoft-evsecurity-cef-user-create-success-4720 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | account_domain |  | ['\sdntdom=({dest_domain}({account_domain}[^\s]+))'] |
| edit_regex_field | account_name |  | ['\sduser=({dest_user}({account_name}.+?))\s+\w+='] |
| added_regex_field | dest_domain |  | ['\sdntdom=({dest_domain}({account_domain}[^\s]+))'] |
| added_regex_field | dest_user |  | ['\sduser=({dest_user}({account_name}.+?))\s+\w+='] |
| removed_attribute | DupFields |  | N/A |