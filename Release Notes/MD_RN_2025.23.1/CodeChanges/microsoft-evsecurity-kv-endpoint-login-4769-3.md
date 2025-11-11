# Code Changes for microsoft-evsecurity-kv-endpoint-login-4769-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_login_id', 'dest_user', 'domain', 'event_code', 'event_id', 'host', 'login_id', 'result_code', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user'] |
| edit_regex_field | domain |  | ['TargetUserName="+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^"]+))"'] |
| edit_regex_field | login_id |  | ['TargetLogonId="+({dest_login_id}({login_id}[^"]+))"'] |
| edit_regex_field | user |  | ['TargetUserName="+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^"]+))"'] |
| added_regex_field | dest_domain |  | ['TargetUserName="+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^"]+))"'] |
| added_regex_field | dest_login_id |  | ['TargetLogonId="+({dest_login_id}({login_id}[^"]+))"'] |
| added_regex_field | dest_user |  | ['TargetUserName="+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |