# Code Changes for pingidentity-pi-json-app-authentication-success-pingid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.actors[0].name,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['exa_json_path=$.actors[0].name,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |