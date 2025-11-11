# Code Changes for microsoft-evsecurity-xml-endpoint-login-success-4770 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'host', 'run_level', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(?=\w)({dest_domain}({domain}[^<]+))</Data>', '<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^<]+))</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>', '<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^<]+))</Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")TargetSid(\'|")>(?:NONE_MAPPED|({dest_user_sid}({user_sid}[^<]+)))</Data>'] |
| added_regex_field | dest_domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(?=\w)({dest_domain}({domain}[^<]+))</Data>', '<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^<]+))</Data>'] |
| added_regex_field | dest_user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>', '<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({dest_domain}({domain}[^<]+))</Data>'] |
| added_regex_field | dest_user_sid |  | ['<Data Name\\*=(\'|")TargetSid(\'|")>(?:NONE_MAPPED|({dest_user_sid}({user_sid}[^<]+)))</Data>'] |
| removed_attribute | DupFields |  | N/A |