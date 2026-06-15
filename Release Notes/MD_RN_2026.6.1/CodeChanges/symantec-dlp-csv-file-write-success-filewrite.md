# Code Changes for symantec-dlp-csv-file-write-success-filewrite (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['User\s*(Name)?:\s+(SYSTEM|None|NETWORK|LOCAL|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),Domain'] |
| edit_regex_field | user |  | ['User\s*(Name)?:\s+(SYSTEM|None|NETWORK|LOCAL|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),Domain'] |