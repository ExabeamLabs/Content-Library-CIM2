# Code Changes for microsoft-evsecurity-mix-user-disable-success-4725 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+))<', 'Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\[nrt]\s+|\s+)Account Domain:\s+({domain}.+?)(\\[nrt]\s+|\s+)Logon ID', '\"SubjectDomainName\":\"({domain}[^\"]+)'] |
| edit_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}({src_domain}[^<]+))<'] |
| edit_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<', 'Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\[nrt]\s+|\s+)Account Domain:\s+({domain}.+?)(\\[nrt]\s+|\s+)Logon ID', '\"SubjectUserName\":\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| removed_attribute | DupFields |  | N/A |