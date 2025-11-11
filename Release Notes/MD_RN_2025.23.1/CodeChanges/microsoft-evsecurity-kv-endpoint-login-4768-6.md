# Code Changes for microsoft-evsecurity-kv-endpoint-login-4768-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'host', 'result_code', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['TargetDomainName="+({dest_domain}({domain}[^"]+))"'] |
| edit_regex_field | user |  | ['TargetUserName="+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user_sid |  | ['TargetSid="+({dest_user_sid}({user_sid}[^"]+))"'] |
| added_regex_field | dest_domain |  | ['TargetDomainName="+({dest_domain}({domain}[^"]+))"'] |
| added_regex_field | dest_user |  | ['TargetUserName="+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | dest_user_sid |  | ['TargetSid="+({dest_user_sid}({user_sid}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |