# Code Changes for microsoft-evsecurity-xml-user-privilege-use-success-4674 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+?))<', '<Data Name\\*=(\'|")SubjectUserSid(\'|")>\s*(({domain}[^\\<]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<'] |
| edit_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+?))<'] |
| edit_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<', '<Data Name\\*=(\'|")SubjectUserSid(\'|")>\s*(({domain}[^\\<]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<'] |
| removed_attribute | DupFields |  | N/A |