# Code Changes for mcafee-sncasb-cef-alert-trigger-success-superhumanalertaccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['suser=(N\/A|system:anonymous|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s', 'usrName=(({email_address}[^@]+@[^@\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | email_domain |  | ['suser=(N\/A|system:anonymous|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s'] |
| edit_regex_field | user |  | ['suser=(N\/A|system:anonymous|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s', 'usrName=(({email_address}[^@]+@[^@\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |