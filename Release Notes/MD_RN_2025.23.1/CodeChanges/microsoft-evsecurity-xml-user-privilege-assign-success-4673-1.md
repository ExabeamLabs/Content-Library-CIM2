# Code Changes for microsoft-evsecurity-xml-user-privilege-assign-success-4673-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name[\\\/]*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+?))</Data>', '<Data Name[\\\/]*=(\'|")SubjectUserSid(\'|")>\s*(({domain}[^\\\/<]+)[\\\/])?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | src_domain |  | ['<Data Name[\\\/]*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+?))</Data>'] |
| edit_regex_field | src_user |  | ['<Data Name[\\\/]*=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| edit_regex_field | user |  | ['<Data Name[\\\/]*=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>', '<Data Name[\\\/]*=(\'|")SubjectUserSid(\'|")>\s*(({domain}[^\\\/<]+)[\\\/])?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| removed_attribute | DupFields |  | N/A |