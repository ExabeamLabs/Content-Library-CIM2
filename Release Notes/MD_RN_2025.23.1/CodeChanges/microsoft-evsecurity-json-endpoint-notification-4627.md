# Code Changes for microsoft-evsecurity-json-endpoint-notification-4627 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'dest_domain', 'dest_host', 'dest_ip', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"TargetDomainName"+:"+(NT AUTHORITY|({dest_domain}({domain}[^"]+)))'] |
| edit_regex_field | login_id |  | ['"SubjectLogonId"+:"+({dest_login_id}({login_id}[^"]+))', '"TargetLogonId"+:"+({dest_login_id}({login_id}[^"]+))'] |
| edit_regex_field | user |  | ['"TargetUserName"+:"+(SYSTEM|ANONYMOUS|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user_sid |  | ['"SubjectUserSid"+:"+(SYSTEM|NT AUTHORITY|\\NULL SID|({dest_user_sid}({user_sid}[^"]+)))', '"TargetUserSid"+:"+(SYSTEM|ANONYMOUS|({dest_user_sid}({user_sid}[^",]+)))'] |
| added_regex_field | dest_domain |  | ['"TargetDomainName"+:"+(NT AUTHORITY|({dest_domain}({domain}[^"]+)))'] |
| added_regex_field | dest_login_id |  | ['"SubjectLogonId"+:"+({dest_login_id}({login_id}[^"]+))', '"TargetLogonId"+:"+({dest_login_id}({login_id}[^"]+))'] |
| added_regex_field | dest_user |  | ['"TargetUserName"+:"+(SYSTEM|ANONYMOUS|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | dest_user_sid |  | ['"SubjectUserSid"+:"+(SYSTEM|NT AUTHORITY|\\NULL SID|({dest_user_sid}({user_sid}[^"]+)))', '"TargetUserSid"+:"+(SYSTEM|ANONYMOUS|({dest_user_sid}({user_sid}[^",]+)))'] |
| removed_attribute | DupFields |  | N/A |