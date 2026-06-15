# Code Changes for microsoft-mssql-xml-database-login-audit (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Message>.+?user\s\'((({domain}[^\\\']+)\\)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\''] |
| edit_regex_field | email_address |  | ['<Message>.+?user\s\'((({domain}[^\\\']+)\\)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\''] |
| edit_regex_field | user |  | ['<Message>.+?user\s\'((({domain}[^\\\']+)\\)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\''] |