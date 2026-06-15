# Code Changes for forcepoint-dlp-cef-alert-trigger-success-dlpsyslog-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['destination="({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^;\]\s"\\,\|]+)[^"]+)"'] |
| edit_regex_field | email_address |  | ['sourceEmail="({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| edit_regex_field | email_recipients |  | ['destination="({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^;\]\s"\\,\|]+)[^"]+)"'] |