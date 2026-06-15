# Code Changes for microsoft-azure-str-endpoint-login-success-primaryauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\suser\s+\'*(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\'\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\''] |
| edit_regex_field | user |  | ['\suser\s+\'*(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\'\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\''] |