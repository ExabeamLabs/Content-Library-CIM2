# Code Changes for microsoft-azuremfa-str-app-activity-success-user (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['pfsvc: User\s+"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | email_address |  | ['pfsvc: User\s+"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | email_domain |  | ['pfsvc: User\s+"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['pfsvc: User\s+"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |