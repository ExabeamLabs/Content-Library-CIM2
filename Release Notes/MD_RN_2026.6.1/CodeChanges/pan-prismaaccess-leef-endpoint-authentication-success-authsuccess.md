# Code Changes for pan-prismaaccess-leef-endpoint-authentication-success-authsuccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ["user\s*'((({user}[\w\.\-]{1,40}\$?)@({domain}[^']+))|(pre-logon|((({=domain}[^\\']+)\\)?({=user}[^']+))))'", 'usrName=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-]{1,40}\$?))'] |
| edit_regex_field | email_address |  | ['usrName=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-]{1,40}\$?))'] |
| edit_regex_field | user |  | ["user\s*'((({user}[\w\.\-]{1,40}\$?)@({domain}[^']+))|(pre-logon|((({=domain}[^\\']+)\\)?({=user}[^']+))))'", 'usrName=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-]{1,40}\$?))'] |