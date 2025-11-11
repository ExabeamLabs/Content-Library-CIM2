# Code Changes for microsoft-evsecurity-xml-endpoint-login-fail-4771 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'result_code', 'run_level', 'src_ip', 'src_port', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*((({domain}[^<\\]+)\\+)?(null|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))|({user_upn}[\w\.\-\!\#\^\~]{1,40}\$?@[^<]+?))<\/Data>', '<Data Name\\*=(\'|")ServiceName(\'|")>([^\/]+?\/)?({domain}[^<]+)</Data>'] |
| edit_regex_field | result_code |  | ['<Data Name\\*=(\'|")Status(\'|")>({failure_code}({result_code}[^<]+))</Data>'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*((({domain}[^<\\]+)\\+)?(null|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))|({user_upn}[\w\.\-\!\#\^\~]{1,40}\$?@[^<]+?))<\/Data>', '<Data Name\\*=(\'|")TargetUserName(\'|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")TargetSid(\'|")>(?:NONE_MAPPED|({dest_user_sid}({user_sid}[^<]+)))</Data>'] |
| edit_regex_field | user_upn |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*((({domain}[^<\\]+)\\+)?(null|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))|({user_upn}[\w\.\-\!\#\^\~]{1,40}\$?@[^<]+?))<\/Data>'] |
| added_regex_field | dest_user |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*((({domain}[^<\\]+)\\+)?(null|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))|({user_upn}[\w\.\-\!\#\^\~]{1,40}\$?@[^<]+?))<\/Data>', '<Data Name\\*=(\'|")TargetUserName(\'|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| added_regex_field | dest_user_sid |  | ['<Data Name\\*=(\'|")TargetSid(\'|")>(?:NONE_MAPPED|({dest_user_sid}({user_sid}[^<]+)))</Data>'] |
| added_regex_field | failure_code |  | ['<Data Name\\*=(\'|")Status(\'|")>({failure_code}({result_code}[^<]+))</Data>'] |
| removed_attribute | DupFields |  | N/A |