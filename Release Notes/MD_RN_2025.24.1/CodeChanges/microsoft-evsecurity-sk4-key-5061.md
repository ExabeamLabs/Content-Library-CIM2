# Code Changes for microsoft-evsecurity-sk4-key-5061 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))'] |
| edit_regex_field | src_domain |  | ['"+SubjectDomainName"+:"+({src_domain}({domain}[^"]+))', '"+SubjectDomainName"+:"+({src_domain}[^"]+)'] |
| edit_regex_field | src_user |  | ['"+SubjectUserName"+:"+(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '"+SubjectUserName"+:"+(SYSTEM|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['"+SubjectUserName"+:"+(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '"user"+:"+(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |