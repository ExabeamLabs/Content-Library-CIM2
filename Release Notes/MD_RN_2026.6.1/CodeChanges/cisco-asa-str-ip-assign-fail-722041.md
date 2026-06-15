# Code Changes for cisco-asa-str-ip-assign-fail-722041 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | [' User <(({domain}[^\s\\]+)\\+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))>'] |
| edit_regex_field | email_address |  | [' User <(({domain}[^\s\\]+)\\+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))>'] |
| edit_regex_field | user |  | [' User <(({domain}[^\s\\]+)\\+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))>', '\sUser\s*<({user}[\w\.\-\!\#\^\~]{1,40}\$?)>'] |