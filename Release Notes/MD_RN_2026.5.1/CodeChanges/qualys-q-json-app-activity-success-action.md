# Code Changes for qualys-q-json-app-activity-success-action (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.[\'User Name\'],exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}\w+(\s+\w+)+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | full_name |  | ['exa_json_path=$.[\'User Name\'],exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}\w+(\s+\w+)+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['exa_json_path=$.[\'User Name\'],exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}\w+(\s+\w+)+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |