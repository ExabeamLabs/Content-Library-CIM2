# Code Changes for microsoft-evsecurity-kv-endpoint-logout-4634 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_ip', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['Account Domain:\s*({dest_domain}({domain}\S+))\s+Logon ID:', 'exa_json_path=$..TargetDomainName,exa_regex=(-|NT AUTHORITY|({dest_domain}({domain}[^\s\\"]+)))'] |
| edit_regex_field | login_id |  | ['Logon ID:\s*({dest_login_id}({login_id}\S+))\s+Logon Type:'] |
| edit_regex_field | user |  | ['Account Name:\s*(SYSTEM|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+Account Domain:', 'exa_json_path=$..TargetUserName,exa_regex=(SYSTEM|ANONYMOUS LOGON|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user_sid |  | ['Security ID:\s*(SYSTEM|({dest_user_sid}({user_sid}\S+)))\s+Account Name:', 'exa_json_path=$..TargetUserSid,exa_regex=(SYSTEM|({dest_user_sid}({user_sid}\S+)))'] |
| added_regex_field | dest_domain |  | ['Account Domain:\s*({dest_domain}({domain}\S+))\s+Logon ID:', 'exa_json_path=$..TargetDomainName,exa_regex=(-|NT AUTHORITY|({dest_domain}({domain}[^\s\\"]+)))'] |
| added_regex_field | dest_login_id |  | ['Logon ID:\s*({dest_login_id}({login_id}\S+))\s+Logon Type:'] |
| added_regex_field | dest_user |  | ['Account Name:\s*(SYSTEM|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+Account Domain:', 'exa_json_path=$..TargetUserName,exa_regex=(SYSTEM|ANONYMOUS LOGON|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | dest_user_sid |  | ['Security ID:\s*(SYSTEM|({dest_user_sid}({user_sid}\S+)))\s+Account Name:', 'exa_json_path=$..TargetUserSid,exa_regex=(SYSTEM|({dest_user_sid}({user_sid}\S+)))'] |
| removed_attribute | DupFields |  | N/A |