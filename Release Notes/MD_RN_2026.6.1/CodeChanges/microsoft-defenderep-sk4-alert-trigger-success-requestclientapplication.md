# Code Changes for microsoft-defenderep-sk4-alert-trigger-success-requestclientapplication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['InitiatingProcessAccountName"+:\s*"+(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['InitiatingProcessAccountName"+:\s*"+(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|system|local service|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |