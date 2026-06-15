# Code Changes for sentinelone-singularityp-json-configuration-modify-success-actions (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.userName,exa_regex=(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | first_name |  | ['exa_json_path=$.userName,exa_regex=(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | full_name |  | ['exa_json_path=$.userName,exa_regex=(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | last_name |  | ['exa_json_path=$.userName,exa_regex=(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['exa_json_path=$.userName,exa_regex=(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |