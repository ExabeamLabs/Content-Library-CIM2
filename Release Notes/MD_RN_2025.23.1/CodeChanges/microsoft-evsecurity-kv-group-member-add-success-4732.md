# Code Changes for microsoft-evsecurity-kv-group-member-add-success-4732 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'dest_user_sid', 'domain', 'event_code', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'src_host', 'time', 'user', 'user_dn', 'user_ou'] |
| edit_regex_field | event_code |  | ['({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}\d+),(?!\d+)({host}({src_host}[\w\-.]+)),.+?グループにメンバーが追加されました。'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}\d+),(?!\d+)({host}({src_host}[\w\-.]+)),.+?グループにメンバーが追加されました。'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}\d+),(?!\d+)({host}({src_host}[\w\-.]+)),.+?グループにメンバーが追加されました。'] |
| added_regex_field | account_domain |  | ['メンバー:\s+セキュリティ ID:\s+(({dest_user_sid}S-\d+-[^\s"]+)|({account_id}[^\s:"]+))|({account_domain}[^\\]+)\\({account_name}.+?)|(?:.+?))\s+アカウント名:'] |
| added_regex_field | account_id |  | ['メンバー:\s+セキュリティ ID:\s+(({dest_user_sid}S-\d+-[^\s"]+)|({account_id}[^\s:"]+))|({account_domain}[^\\]+)\\({account_name}.+?)|(?:.+?))\s+アカウント名:'] |
| added_regex_field | account_name |  | ['メンバー:\s+セキュリティ ID:\s+(({dest_user_sid}S-\d+-[^\s"]+)|({account_id}[^\s:"]+))|({account_domain}[^\\]+)\\({account_name}.+?)|(?:.+?))\s+アカウント名:'] |
| added_regex_field | dest_user_sid |  | ['メンバー:\s+セキュリティ ID:\s+(({dest_user_sid}S-\d+-[^\s"]+)|({account_id}[^\s:"]+))|({account_domain}[^\\]+)\\({account_name}.+?)|(?:.+?))\s+アカウント名:'] |
| added_regex_field | domain |  | ['アカウント ドメイン:\s+({domain}[^\s]+)'] |
| added_regex_field | group_domain |  | ['グループ:.+?グループ ドメイン:\s+({group_domain}[^\s]+)'] |
| added_regex_field | group_id |  | ['グループ:\s+セキュリティ ID:\s+({group_id}[^\s]+)'] |
| added_regex_field | group_name |  | ['グループ:.+?アカウント名:\s+({group_name}.+?)?\s+アカウント ドメイン:', 'グループ:.+?グループ名:\s+({group_name}.+?)?\s+グループ ドメイン:'] |
| added_regex_field | group_type |  | ['セキュリティが有効な({group_type}[^\s]+)\s+グループにメンバーが追加されました。'] |
| added_regex_field | login_id |  | ['ログオン ID:\s+({login_id}[^\s]+)\s+'] |
| added_regex_field | src_host |  | ['({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),({event_code}\d+),(?!\d+)({host}({src_host}[\w\-.]+)),.+?グループにメンバーが追加されました。'] |
| added_regex_field | user |  | ['サブジェクト:.+?アカウント名:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| added_regex_field | user_dn |  | ['メンバー:.+?アカウント名:\s*({user_dn}(?i)(cn)=.+?,({user_ou}OU.+?DC=[\w-]+))\s*グループ:'] |
| added_regex_field | user_ou |  | ['メンバー:.+?アカウント名:\s*({user_dn}(?i)(cn)=.+?,({user_ou}OU.+?DC=[\w-]+))\s*グループ:'] |
| removed_attribute | DupFields |  | N/A |