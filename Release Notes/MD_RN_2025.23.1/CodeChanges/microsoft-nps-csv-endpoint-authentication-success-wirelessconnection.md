# Code Changes for microsoft-nps-csv-endpoint-authentication-success-wirelessconnection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | [',4129,({domain}[^\\]+)?(\\\\?)(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))?,?'] |
| edit_regex_field | email_address |  | [',4129,({domain}[^\\]+)?(\\\\?)(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))?,?'] |
| edit_regex_field | email_domain |  | [',4129,({domain}[^\\]+)?(\\\\?)(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))?,?'] |
| edit_regex_field | user |  | [',4129,({domain}[^\\]+)?(\\\\?)(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))?,?'] |