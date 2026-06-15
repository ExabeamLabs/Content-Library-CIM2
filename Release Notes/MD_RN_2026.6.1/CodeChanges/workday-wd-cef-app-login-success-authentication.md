# Code Changes for workday-wd-cef-app-login-success-authentication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\"userName\":\"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^\s,]+([\s,]+\s*[^\s"]+)+?))\"'] |
| edit_regex_field | full_name |  | ['\"userName\":\"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^\s,]+([\s,]+\s*[^\s"]+)+?))\"'] |
| edit_regex_field | user |  | ['\"userName\":\"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^\s,]+([\s,]+\s*[^\s"]+)+?))\"'] |