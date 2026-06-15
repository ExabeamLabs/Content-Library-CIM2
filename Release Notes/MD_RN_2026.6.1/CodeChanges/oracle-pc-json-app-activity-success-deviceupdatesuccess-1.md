# Code Changes for oracle-pc-json-app-activity-success-deviceupdatesuccess-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_regex=actorName\":\"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_regex=idcsLastModifiedBy\":.+?display\":\"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}[^,"\\]+,[^"\\]+))'] |
| edit_regex_field | full_name |  | ['exa_regex=idcsLastModifiedBy\":.+?display\":\"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}[^,"\\]+,[^"\\]+))'] |
| edit_regex_field | user |  | ['exa_regex=actorName\":\"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |