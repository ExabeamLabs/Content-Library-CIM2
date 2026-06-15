# Code Changes for crowdstrike-falcon-cef-app-login-authactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['\Wduser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@]+?))?)\s*(\w+=|$)'] |
| edit_regex_field | email_address |  | ['\Wduser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@]+?))?)\s*(\w+=|$)'] |
| edit_regex_field | email_domain |  | ['\Wduser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@]+?))?)\s*(\w+=|$)'] |
| edit_regex_field | user |  | ['\Wduser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@]+?))?)\s*(\w+=|$)'] |