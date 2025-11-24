# Code Changes for microsoft-windows-json-user-lock-success-4740-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['SubjectDomainName\\?"+:\\?"({domain}({src_domain}[^\\"]+))\\?"', 'SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}({domain}[^\\]+)))\\?"', 'TargetDomainName\\?"+:\\?"({domain}[^\s\\]+)\\?"'] |
| edit_regex_field | src_domain |  | ['SubjectDomainName\\?"+:\\?"({domain}({src_domain}[^\\"]+))\\?"', 'SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}({domain}[^\\]+)))\\?"'] |
| edit_regex_field | src_user |  | ['SubjectUserName\\?"+:\\?"(?:-|LOCAL SYSTEM|({src_user}[^\\]+))\\?"', 'SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?"'] |