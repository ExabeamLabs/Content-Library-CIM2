# Code Changes for microsoft-evntlm-xml-endpoint-login-fail-8004 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['Name=(\'|")DomainName(\'|")>(NULL|({domain}[^<>]+))<'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)\''] |
| edit_regex_field | resource |  | ['Name=(\'|")SChannelName(\'|")>({resource}[^<>]+)<'] |
| edit_regex_field | src_host |  | ['Name=(\'|")WorkstationName(\'|")>\\*(NULL|({src_host}[^<>]+))<'] |
| edit_regex_field | user |  | ['Name=(\'|")UserName(\'|")>(({user_upn}[^@\s<>]+@[^@\s<>]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*<'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^<>\/"\']+)'] |
| edit_regex_field | user_upn |  | ['Name=(\'|")UserName(\'|")>(({user_upn}[^@\s<>]+@[^@\s<>]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*<'] |