# Code Changes for cisco-asa-str-vpn-logout-722012 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['\sUser\s*<(({domain}[^\\>]+)\\)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))>'] |
| edit_regex_field | email_address |  | ['\sUser\s*<(({domain}[^\\>]+)\\)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))>'] |
| edit_regex_field | user |  | ['\sUser\s*<(({domain}[^\\>]+)\\)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))>', '\sUser\s*<({user}[\w\.\-\!\#\^\~]{1,40}\$?)>'] |