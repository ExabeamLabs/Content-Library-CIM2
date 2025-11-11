# Code Changes for microsoft-evsecurity-mix-user-password-modify-4723 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'Account Domain:\s*({domain}[^:]+?)(\\[nrt]\s+|\s+)Logon ID:\s*({login_id}\w+)', 'SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}({src_domain}[^\\"]+)))\\?"', '\Wduser=(({domain}[^\\=]+)\\+)?({dest_user}[^\s\\=]+)', '\Wsntdom=({domain}.+?)(\\[nrt]\s+|\s+)(\w+=|$)', '\Wsuser=(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| edit_regex_field | src_domain |  | ['SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}({src_domain}[^\\"]+)))\\?"'] |
| edit_regex_field | src_user |  | ['SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| edit_regex_field | user |  | ['"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'Subject.+?Account Name:\s*(\\r|\\n|\\t)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\r|\\n|\\t)*\s*Account Domain', 'SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"', '\Wsuser=(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| removed_attribute | DupFields |  | N/A |