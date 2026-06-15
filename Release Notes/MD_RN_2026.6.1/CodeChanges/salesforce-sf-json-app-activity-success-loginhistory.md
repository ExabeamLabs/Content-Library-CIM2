# Code Changes for salesforce-sf-json-app-activity-success-loginhistory (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | db_user |  | ['exa_json_path=$.USER_NAME,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({db_user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.USER_NAME,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({db_user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |