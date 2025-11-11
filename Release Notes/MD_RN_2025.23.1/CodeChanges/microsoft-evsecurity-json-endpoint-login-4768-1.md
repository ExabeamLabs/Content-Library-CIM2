# Code Changes for microsoft-evsecurity-json-endpoint-login-4768-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'process_id', 'result', 'result_code', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"TargetDomainName"+:"+({dest_domain}({domain}[^"]+))"'] |
| edit_regex_field | user |  | ['"TargetUserName"+:"+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_regex=Account Name:\s*({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_domain |  | ['"TargetDomainName"+:"+({dest_domain}({domain}[^"]+))"'] |
| added_regex_field | dest_user |  | ['"TargetUserName"+:"+({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_regex=Account Name:\s*({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |