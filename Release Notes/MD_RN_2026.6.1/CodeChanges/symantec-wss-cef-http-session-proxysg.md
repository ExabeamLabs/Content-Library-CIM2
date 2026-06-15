# Code Changes for symantec-wss-cef-http-session-proxysg (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\ssuser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s\w+='] |
| edit_regex_field | orig_user |  | ['\ssuser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s\w+='] |
| edit_regex_field | user |  | ['\ssuser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s\w+='] |