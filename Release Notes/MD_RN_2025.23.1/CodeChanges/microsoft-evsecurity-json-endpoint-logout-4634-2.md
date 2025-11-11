# Code Changes for microsoft-evsecurity-json-endpoint-logout-4634-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'result', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"TargetDomainName":"({dest_domain}({domain}[^"]+))"'] |
| edit_regex_field | login_id |  | ['"TargetLogonId":"({dest_login_id}({login_id}[^"]+))"'] |
| edit_regex_field | user |  | ['"TargetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_json_path=$..TargetUserName,exa_regex=^({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| edit_regex_field | user_sid |  | ['"TargetUserSid":"({dest_user_sid}({user_sid}[^"]+))"'] |
| added_regex_field | dest_domain |  | ['"TargetDomainName":"({dest_domain}({domain}[^"]+))"'] |
| added_regex_field | dest_login_id |  | ['"TargetLogonId":"({dest_login_id}({login_id}[^"]+))"'] |
| added_regex_field | dest_user |  | ['"TargetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_json_path=$..TargetUserName,exa_regex=^({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| added_regex_field | dest_user_sid |  | ['"TargetUserSid":"({dest_user_sid}({user_sid}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |