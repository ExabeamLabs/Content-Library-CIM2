# Code Changes for microsoft-evsecurity-str-endpoint-notification-4627 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['New Logon:[^"]+?Account Name:\s*(SYSTEM|ANONYMOUS|(({email_address}([A-Za-z0-9]+[!#$%&\'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\w+\s\w+:'] |
| edit_regex_field | user |  | ['Account Name(:|=)\s*(-|SYSTEM|(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*Account Domain', 'New Logon:[^"]+?Account Name:\s*(SYSTEM|ANONYMOUS|(({email_address}([A-Za-z0-9]+[!#$%&\'+\-\.\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\w+\s\w+:'] |