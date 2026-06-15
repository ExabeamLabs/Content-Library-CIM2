# Code Changes for zscaler-ia-cef-http-session-spriv (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['login=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\s\w+=', 'suser=((noauth-protocol[^=]+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)\s)|((\w+[^=]+\->\w+[^=]+)\s|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['suser=((noauth-protocol[^=]+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)\s)|((\w+[^=]+\->\w+[^=]+)\s|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', 'suser=(NA|None|\$NULL|(\w+[^=]+\->\w+[^=]+)\s|(?![^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\w+=|$)'] |