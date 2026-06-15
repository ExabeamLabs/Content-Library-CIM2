# Code Changes for microsoft-evsecurity-json-endpoint-login-680-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['(?:Success|Audit)\s+\w+\s+[^\s.]+(\.({domain}[^\s.]+)[^\s]*)', '(Information|Audit Success|Success Audit|Audit Failure|Failure Audit)\s+[^\s.]+\.({domain}[^\s.]+)', 'Logon (?:a|A)ccount:(?:\s+Source Workstation|\s*(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({domain}[^\s.]+).*?)?\s*Source Workstation)'] |
| edit_regex_field | user |  | ['Logon (?:a|A)ccount:(?:\s+Source Workstation|\s*(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({domain}[^\s.]+).*?)?\s*Source Workstation)'] |
| edit_regex_field | user_upn |  | ['Logon (?:a|A)ccount:(?:\s+Source Workstation|\s*(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(?:@({domain}[^\s.]+).*?)?\s*Source Workstation)'] |