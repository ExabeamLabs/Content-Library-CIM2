# Code Changes for microsoft-evsecurity-cef-endpoint-login-fail-4625 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['\sduser=\s*(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user_upn |  | ['\sduser=\s*(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |