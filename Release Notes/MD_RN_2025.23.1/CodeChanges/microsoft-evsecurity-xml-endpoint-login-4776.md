# Code Changes for microsoft-evsecurity-xml-endpoint-login-4776 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_user', 'domain', 'error_code', 'event_code', 'event_name', 'failure_code', 'host', 'login_type_text', 'result', 'result_code', 'run_level', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_upn'] |
| edit_regex_field | domain |  | ['<Computer>(?!(?:[A-Fa-f:\d.]+))[^<.]+(\.({dest_domain}({domain}[^<]+))[^<]*)?</Computer>', '<Computer>(\w+\.({dest_domain}({domain}[^<]+)))', '<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*((({dest_domain}({domain}[^<\\]+))\\+)?(null|-|NA|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))|({user_upn}[\w\.\-\!\#\^\~]{1,40}\$?@[^<]+?))<\/Data>'] |
| edit_regex_field | result_code |  | ['<Data Name(\\)?=(\'|")Status(\'|")>((?-i)\\+[rnt])*\s*({failure_code}({error_code}({result_code}[^<]+)))<\/Data>'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*((({dest_domain}({domain}[^<\\]+))\\+)?(null|-|NA|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))|({user_upn}[\w\.\-\!\#\^\~]{1,40}\$?@[^<]+?))<\/Data>'] |
| edit_regex_field | user_upn |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*((({dest_domain}({domain}[^<\\]+))\\+)?(null|-|NA|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))|({user_upn}[\w\.\-\!\#\^\~]{1,40}\$?@[^<]+?))<\/Data>'] |
| added_regex_field | dest_domain |  | ['<Computer>(?!(?:[A-Fa-f:\d.]+))[^<.]+(\.({dest_domain}({domain}[^<]+))[^<]*)?</Computer>', '<Computer>(\w+\.({dest_domain}({domain}[^<]+)))', '<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*((({dest_domain}({domain}[^<\\]+))\\+)?(null|-|NA|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))|({user_upn}[\w\.\-\!\#\^\~]{1,40}\$?@[^<]+?))<\/Data>'] |
| added_regex_field | dest_user |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*((({dest_domain}({domain}[^<\\]+))\\+)?(null|-|NA|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))|({user_upn}[\w\.\-\!\#\^\~]{1,40}\$?@[^<]+?))<\/Data>'] |
| added_regex_field | error_code |  | ['<Data Name(\\)?=(\'|")Status(\'|")>((?-i)\\+[rnt])*\s*({failure_code}({error_code}({result_code}[^<]+)))<\/Data>'] |
| added_regex_field | failure_code |  | ['<Data Name(\\)?=(\'|")Status(\'|")>((?-i)\\+[rnt])*\s*({failure_code}({error_code}({result_code}[^<]+)))<\/Data>'] |
| removed_attribute | DupFields |  | N/A |