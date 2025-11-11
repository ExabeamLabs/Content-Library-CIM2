# Code Changes for microsoft-evsecurity-sk4-endpoint-logout-success-anaccountwasloggedoff (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_domain', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"targetDomainName":"({dest_domain}({domain}[^"\s]+?))\s*"'] |
| edit_regex_field | login_id |  | ['"targetLogonId":"({dest_login_id}({login_id}[^"\s]+?))\s*"'] |
| edit_regex_field | user |  | ['"targetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| edit_regex_field | user_sid |  | ['"targetUserSid":"({dest_user_sid}({user_sid}[^"\s]+?))\s*"'] |
| added_regex_field | dest_domain |  | ['"targetDomainName":"({dest_domain}({domain}[^"\s]+?))\s*"'] |
| added_regex_field | dest_login_id |  | ['"targetLogonId":"({dest_login_id}({login_id}[^"\s]+?))\s*"'] |
| added_regex_field | dest_user |  | ['"targetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| added_regex_field | dest_user_sid |  | ['"targetUserSid":"({dest_user_sid}({user_sid}[^"\s]+?))\s*"'] |
| removed_attribute | DupFields |  | N/A |