# Code Changes for microsoft-evsecurity-kv-user-create-success-624 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | account_domain |  | ['New Account Name:\s+({dest_user}({account_name}.+?))\s+New Domain:\s+({account_domain}[^\s]+)\s+New Account ID:\s+(%\{)?({account_id}[^\s\}]+)'] |
| edit_regex_field | account_id |  | ['New Account Name:\s+({dest_user}({account_name}.+?))\s+New Domain:\s+({account_domain}[^\s]+)\s+New Account ID:\s+(%\{)?({account_id}[^\s\}]+)'] |
| edit_regex_field | account_name |  | ['New Account Name:\s+({dest_user}({account_name}.+?))\s+New Domain:\s+({account_domain}[^\s]+)\s+New Account ID:\s+(%\{)?({account_id}[^\s\}]+)'] |
| added_regex_field | dest_user |  | ['New Account Name:\s+({dest_user}({account_name}.+?))\s+New Domain:\s+({account_domain}[^\s]+)\s+New Account ID:\s+(%\{)?({account_id}[^\s\}]+)'] |
| removed_attribute | DupFields |  | N/A |