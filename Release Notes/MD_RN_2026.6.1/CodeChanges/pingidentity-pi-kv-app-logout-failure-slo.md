# Code Changes for pingidentity-pi-kv-app-logout-failure-slo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\ssubject="?(||(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\-\s"\\,;\|]+\.[^\]\s"\\,;\|\-]+))|(?:[^"]+?:)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\-[^"]+)?"?(,|\s\w+=)'] |
| edit_regex_field | email_domain |  | ['\ssubject="?(||(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\-\s"\\,;\|]+\.[^\]\s"\\,;\|\-]+))|(?:[^"]+?:)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\-[^"]+)?"?(,|\s\w+=)'] |
| edit_regex_field | user |  | ['\ssubject="?(||(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\-\s"\\,;\|]+\.[^\]\s"\\,;\|\-]+))|(?:[^"]+?:)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\-[^"]+)?"?(,|\s\w+=)'] |