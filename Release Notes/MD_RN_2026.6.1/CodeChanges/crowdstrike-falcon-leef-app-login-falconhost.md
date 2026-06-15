# Code Changes for crowdstrike-falcon-leef-app-login-falconhost (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['\WusrName=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@]+?))?)(\s*\||\s+\w+=|\s*$|\s*")'] |
| edit_regex_field | email_address |  | ['\WusrName=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@]+?))?)(\s*\||\s+\w+=|\s*$|\s*")'] |
| edit_regex_field | email_domain |  | ['\WusrName=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@]+?))?)(\s*\||\s+\w+=|\s*$|\s*")'] |
| edit_regex_field | user |  | ['\WusrName=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@]+?))?)(\s*\||\s+\w+=|\s*$|\s*")'] |