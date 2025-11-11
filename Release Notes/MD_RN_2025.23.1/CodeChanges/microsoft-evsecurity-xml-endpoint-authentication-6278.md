# Code Changes for microsoft-evsecurity-xml-endpoint-authentication-6278 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+))</Data>', 'Account Domain:\s*(NT AUTHORITY|({domain}\S+))\s+Logon ID:'] |
| edit_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+))</Data>'] |
| edit_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>', 'Account Name:\s*(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:'] |
| edit_regex_field | user_upn |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| removed_attribute | DupFields |  | N/A |