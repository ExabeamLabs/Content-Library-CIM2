# Code Changes for microsoft-evsecurity-kv-user-delete-fail-locked (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'src_domain', 'src_host', 'src_user', 'user', 'user_sid'] |
| edit_regex_field | login_id |  | ['Subject:.+?Account Name:\s+({src_user}.+?)\s+Account Domain:\s+(?=\w)({domain}({src_domain}.+?))\s+Logon ID:\s+({login_id}[^\s]+)'] |
| edit_regex_field | src_domain |  | ['Subject:.+?Account Name:\s+({src_user}.+?)\s+Account Domain:\s+(?=\w)({domain}({src_domain}.+?))\s+Logon ID:\s+({login_id}[^\s]+)'] |
| edit_regex_field | src_user |  | ['Subject:.+?Account Name:\s+({src_user}.+?)\s+Account Domain:\s+(?=\w)({domain}({src_domain}.+?))\s+Logon ID:\s+({login_id}[^\s]+)'] |
| added_regex_field | domain |  | ['Subject:.+?Account Name:\s+({src_user}.+?)\s+Account Domain:\s+(?=\w)({domain}({src_domain}.+?))\s+Logon ID:\s+({login_id}[^\s]+)'] |
| removed_attribute | DupFields |  | N/A |