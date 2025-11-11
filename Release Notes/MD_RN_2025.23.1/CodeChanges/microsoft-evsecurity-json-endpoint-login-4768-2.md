# Code Changes for microsoft-evsecurity-json-endpoint-login-4768-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'result_code', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['TargetDomainNam":"(?:-|({dest_domain}({domain}[^"]+?)))"'] |
| edit_regex_field | user |  | ['TargetUserName":"(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| edit_regex_field | user_sid |  | ['TargetSid":"({dest_user_sid}({user_sid}[^"\\]+))"'] |
| added_regex_field | dest_domain |  | ['TargetDomainNam":"(?:-|({dest_domain}({domain}[^"]+?)))"'] |
| added_regex_field | dest_user |  | ['TargetUserName":"(?:-|(?i)(system|anonymous logon|LOCAL SERVICE|LOCAL SYSTEM)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | dest_user_sid |  | ['TargetSid":"({dest_user_sid}({user_sid}[^"\\]+))"'] |
| removed_attribute | DupFields |  | N/A |