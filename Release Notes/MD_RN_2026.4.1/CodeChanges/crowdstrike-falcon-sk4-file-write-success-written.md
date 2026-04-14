# Code Changes for crowdstrike-falcon-sk4-file-write-success-written (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"UserName":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+)))"'] |
| edit_regex_field | first_name |  | ['"UserName":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+)))"'] |
| edit_regex_field | full_name |  | ['"UserName":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+)))"'] |
| edit_regex_field | last_name |  | ['"UserName":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+)))"'] |
| edit_regex_field | user |  | ['"UserName":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+)))"'] |