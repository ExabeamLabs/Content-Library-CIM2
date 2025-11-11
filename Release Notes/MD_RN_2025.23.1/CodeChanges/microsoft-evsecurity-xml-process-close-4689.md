# Code Changes for microsoft-evsecurity-xml-process-close-4689 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>(-|({domain}[^<]+?))<', '<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+))', 'Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:'] |
| edit_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+))'] |
| edit_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<', '<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', 'Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:'] |
| removed_attribute | DupFields |  | N/A |