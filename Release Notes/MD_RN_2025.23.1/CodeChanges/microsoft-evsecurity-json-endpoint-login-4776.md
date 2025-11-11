# Code Changes for microsoft-evsecurity-json-endpoint-login-4776 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_id', 'event_name', 'failure_code', 'host', 'login_type_text', 'result', 'result_code', 'src_host', 'time', 'user', 'user_upn'] |
| edit_regex_field | domain |  | ['"(Hostname|MachineName)":"(?!(?:[A-Fa-f:\d.]+))[^."]*\.({dest_domain}({domain}[^.]*))', '"TargetUserName":"[^"@]+(?:@({dest_domain}({domain}[^"@\s]+))[^"]*)?'] |
| edit_regex_field | result_code |  | ['"Status":"({failure_code}({result_code}[^"]*))"'] |
| edit_regex_field | user |  | ['"TargetUserName":"(({user_upn}[^@"]+@[^\."]+(\.[^"]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user_upn |  | ['"TargetUserName":"(({user_upn}[^@"]+@[^\."]+(\.[^"]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | dest_domain |  | ['"(Hostname|MachineName)":"(?!(?:[A-Fa-f:\d.]+))[^."]*\.({dest_domain}({domain}[^.]*))', '"TargetUserName":"[^"@]+(?:@({dest_domain}({domain}[^"@\s]+))[^"]*)?'] |
| added_regex_field | dest_user |  | ['"TargetUserName":"(({user_upn}[^@"]+@[^\."]+(\.[^"]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | failure_code |  | ['"Status":"({failure_code}({result_code}[^"]*))"'] |
| removed_attribute | DupFields |  | N/A |