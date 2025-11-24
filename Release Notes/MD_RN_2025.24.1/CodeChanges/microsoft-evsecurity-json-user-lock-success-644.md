# Code Changes for microsoft-evsecurity-json-user-lock-success-644 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | login_id |  | ['Caller User Name:\s+({src_user}.+?)\s+Caller Domain:\s+(?=\w)({domain}({src_domain}.+?))\s+Caller Logon ID:\s+\([^,]+,({login_id}[^\)]+)'] |
| edit_regex_field | src_domain |  | ['Caller User Name:\s+({src_user}.+?)\s+Caller Domain:\s+(?=\w)({domain}({src_domain}.+?))\s+Caller Logon ID:\s+\([^,]+,({login_id}[^\)]+)'] |
| edit_regex_field | src_user |  | ['Caller User Name:\s+({src_user}.+?)\s+Caller Domain:\s+(?=\w)({domain}({src_domain}.+?))\s+Caller Logon ID:\s+\([^,]+,({login_id}[^\)]+)'] |
| added_regex_field | domain |  | ['Caller User Name:\s+({src_user}.+?)\s+Caller Domain:\s+(?=\w)({domain}({src_domain}.+?))\s+Caller Logon ID:\s+\([^,]+,({login_id}[^\)]+)'] |
| removed_attribute | DupFields |  | N/A |