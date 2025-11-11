# Code Changes for microsoft-evsecurity-mix-endpoint-login-4769-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_user', 'domain', 'event_code', 'host', 'result_code', 'service_name', 'src_ip', 'src_port', 'ticket_encryption_type', 'ticket_options', 'time', 'user'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(?=\w)({dest_domain}({domain}[^<]+))</Data>', '<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({dest_domain}({domain}[^<]+)))?</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({dest_domain}({domain}[^<]+)))?</Data>'] |
| added_regex_field | dest_domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(?=\w)({dest_domain}({domain}[^<]+))</Data>', '<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({dest_domain}({domain}[^<]+)))?</Data>'] |
| added_regex_field | dest_user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({dest_domain}({domain}[^<]+)))?</Data>'] |
| removed_attribute | DupFields |  | N/A |