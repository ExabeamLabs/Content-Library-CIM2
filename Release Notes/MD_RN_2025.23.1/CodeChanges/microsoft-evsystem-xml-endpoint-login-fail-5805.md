# Code Changes for microsoft-evsystem-xml-endpoint-login-fail-5805 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['"Domain"*:"*({domain}[^"]+)', '"SubjectDomainName"*:"*({domain}({src_domain}[^"]+))"'] |
| edit_regex_field | src_domain |  | ['"SubjectDomainName"*:"*({domain}({src_domain}[^"]+))"'] |
| edit_regex_field | src_user |  | ['"SubjectUserName"*:"*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['"AccountName"*:"*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', '"SubjectUserName"*:"*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |