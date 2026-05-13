# Code Changes for microsoft-evsecurity-cef-endpoint-authentication-success-4768 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['\sduser=\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user_upn |  | ['\sduser=\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |