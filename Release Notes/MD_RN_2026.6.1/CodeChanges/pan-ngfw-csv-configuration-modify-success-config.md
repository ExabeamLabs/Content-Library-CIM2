# Code Changes for pan-ngfw-csv-configuration-modify-success-config (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | [',CONFIG,.+?\d\d:\d\d:\d\d([^,]*,){4}(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| edit_regex_field | user |  | [',CONFIG,.+?\d\d:\d\d:\d\d([^,]*,){4}(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |