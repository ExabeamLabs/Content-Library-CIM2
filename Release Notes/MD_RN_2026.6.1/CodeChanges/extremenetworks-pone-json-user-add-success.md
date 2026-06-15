# Code Changes for extremenetworks-pone-json-user-add-success (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.email,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_json_path=$.username,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}\w+(\s+\w+)+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | full_name |  | ['exa_json_path=$.username,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}\w+(\s+\w+)+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['exa_json_path=$.email,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_json_path=$.username,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}\w+(\s+\w+)+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |