# Code Changes for microsoft-evsecurity-kv-process-close-processexited (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"', '(Primary)? User Name\s*:\s*(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(Primary)? Domain\s*:\s*(-|({domain}[^\s]+))\s', 'Account Domain:\s*({src_domain}({domain}[^:]+?))\s+Logon ID:'] |
| edit_regex_field | src_domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"', 'Account Domain:\s*({src_domain}({domain}[^:]+?))\s+Logon ID:', 'Caller User Name\s*:\s*(-|({src_user}.+?))\s+Caller Domain\s*:\s*(-|({src_domain}.+?))\s+Caller Logon ID\s*:\s*(-|({login_id}[^\s]+))'] |
| edit_regex_field | src_user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'Account Name:\s*[\\t\\r\\n]*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'Caller User Name\s*:\s*(-|({src_user}.+?))\s+Caller Domain\s*:\s*(-|({src_domain}.+?))\s+Caller Logon ID\s*:\s*(-|({login_id}[^\s]+))'] |
| edit_regex_field | user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', '(Primary)? User Name\s*:\s*(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(Primary)? Domain\s*:\s*(-|({domain}[^\s]+))\s', 'Account Name:\s*[\\t\\r\\n]*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'User=(NOT_TRANSLATED|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |