# Code Changes for microsoft-evsecurity-kv-user-create-success-4720-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'computer_name', 'dest_domain', 'dest_user', 'domain', 'event_code', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | account_domain |  | ['新しいアカウント:.+?セキュリティ ID:\s+({account_id}[^\s]+)\s+アカウント名:\s+({dest_user}({account_name}.+?))\s+アカウント ドメイン:\s+({dest_domain}({account_domain}[^\s]+))'] |
| edit_regex_field | account_id |  | ['新しいアカウント:.+?セキュリティ ID:\s+({account_id}[^\s]+)\s+アカウント名:\s+({dest_user}({account_name}.+?))\s+アカウント ドメイン:\s+({dest_domain}({account_domain}[^\s]+))'] |
| edit_regex_field | account_name |  | ['新しいアカウント:.+?セキュリティ ID:\s+({account_id}[^\s]+)\s+アカウント名:\s+({dest_user}({account_name}.+?))\s+アカウント ドメイン:\s+({dest_domain}({account_domain}[^\s]+))'] |
| edit_regex_field | computer_name |  | ['ComputerName=({computer_name}({host}[\w.\-]+))'] |
| edit_regex_field | host |  | ['(?!\d+)({host}[\w\-.]+),([^,]*,)?ユーザー アカウントが作成されました。', 'ComputerName=({computer_name}({host}[\w.\-]+))'] |
| added_regex_field | dest_domain |  | ['新しいアカウント:.+?セキュリティ ID:\s+({account_id}[^\s]+)\s+アカウント名:\s+({dest_user}({account_name}.+?))\s+アカウント ドメイン:\s+({dest_domain}({account_domain}[^\s]+))'] |
| added_regex_field | dest_user |  | ['新しいアカウント:.+?セキュリティ ID:\s+({account_id}[^\s]+)\s+アカウント名:\s+({dest_user}({account_name}.+?))\s+アカウント ドメイン:\s+({dest_domain}({account_domain}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |