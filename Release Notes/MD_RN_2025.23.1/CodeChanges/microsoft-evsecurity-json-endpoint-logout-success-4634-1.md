# Code Changes for microsoft-evsecurity-json-endpoint-logout-success-4634-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"+TargetDomainName"+:"+({dest_domain}({domain}[^"]+))"+', 'Account Domain:\s*({dest_domain}({domain}\S+))\s+Logon ID:'] |
| edit_regex_field | login_id |  | ['"+TargetLogonId"+:"+({dest_login_id}({login_id}[^"]+))"+'] |
| edit_regex_field | user |  | ['"+TargetUserName"+:"+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"+', 'Account Name:\s*(SYSTEM|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+Account Domain:'] |
| edit_regex_field | user_sid |  | ['"+TargetUserSid"+:"+({dest_user_sid}({user_sid}[^"]+))"+', 'Security ID:\s*(SYSTEM|({dest_user_sid}({user_sid}\S+)))\s+Account Name:'] |
| added_regex_field | dest_domain |  | ['"+TargetDomainName"+:"+({dest_domain}({domain}[^"]+))"+', 'Account Domain:\s*({dest_domain}({domain}\S+))\s+Logon ID:'] |
| added_regex_field | dest_login_id |  | ['"+TargetLogonId"+:"+({dest_login_id}({login_id}[^"]+))"+'] |
| added_regex_field | dest_user |  | ['"+TargetUserName"+:"+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"+', 'Account Name:\s*(SYSTEM|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+Account Domain:'] |
| added_regex_field | dest_user_sid |  | ['"+TargetUserSid"+:"+({dest_user_sid}({user_sid}[^"]+))"+', 'Security ID:\s*(SYSTEM|({dest_user_sid}({user_sid}\S+)))\s+Account Name:'] |
| removed_attribute | DupFields |  | N/A |