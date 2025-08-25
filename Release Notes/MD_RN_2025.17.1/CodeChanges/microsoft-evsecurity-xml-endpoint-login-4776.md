# Code Changes for microsoft-evsecurity-xml-endpoint-login-4776 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Computer>(?!(?:[A-Fa-f:\d.]+))[^<.]+(\.({domain}[^<]+)[^<]*)?</Computer>', '<Computer>(\w+\.({domain}[^<]+))', '<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*((({domain}[^<\\]+)\\+)?(null|-|NA|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({user_upn}[\w\.\-\!\#\^\~]{1,40}\$?@[^<]+?))<\/Data>'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*((({domain}[^<\\]+)\\+)?(null|-|NA|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({user_upn}[\w\.\-\!\#\^\~]{1,40}\$?@[^<]+?))<\/Data>'] |
| edit_regex_field | user_upn |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*((({domain}[^<\\]+)\\+)?(null|-|NA|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({user_upn}[\w\.\-\!\#\^\~]{1,40}\$?@[^<]+?))<\/Data>'] |