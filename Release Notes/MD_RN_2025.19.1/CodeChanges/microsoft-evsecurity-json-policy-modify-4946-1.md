# Code Changes for microsoft-evsecurity-json-policy-modify-4946-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_name', 'login_id', 'rule', 'rule_id', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['exa_json_path=$.UserID,exa_regex=(({user_sid}S-[^"]+?)|(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_regex=Account Domain:\s+({domain}[^\s]+)', 'exa_regex=Account Name:\s*(({domain}[^:\\]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+){1,2}:\s'] |
| edit_regex_field | rule |  | ['exa_regex=Rule Name:\s*({rule}[^":]+)'] |
| edit_regex_field | rule_id |  | ['exa_regex=Rule ID:\s*({rule_id}[^\s]+)'] |
| edit_regex_field | user |  | ['exa_json_path=$.UserID,exa_regex=(({user_sid}S-[^"]+?)|(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_regex=Account Name:\s*(({domain}[^:\\]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+){1,2}:\s'] |
| edit_regex_field | user_sid |  | ['exa_json_path=$.UserID,exa_regex=(({user_sid}S-[^"]+?)|(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_regex=Subject:\s+Security ID:\s+({user_sid}[^\s]+)'] |
| added_regex_field | login_id |  | ['exa_regex=Logon ID:\s+({login_id}[^\s]+)'] |