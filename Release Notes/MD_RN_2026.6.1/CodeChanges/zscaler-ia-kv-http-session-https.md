# Code Changes for zscaler-ia-kv-http-session-https (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\suser=((\w+[^=]+\->\w+[^=]+)|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)'] |
| edit_regex_field | user |  | ['\suser=((\w+[^=]+\->\w+[^=]+)|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)', '\suser=(?![^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\w+=|$)'] |