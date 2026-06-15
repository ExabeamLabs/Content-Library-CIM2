# Code Changes for microsoft-evsystem-xml-endpoint-activity-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['<Data Name=(\'|")AccountName(\'|")>(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|<]+\.[^\]\s"\\,\|<]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^<]+))<'] |
| edit_regex_field | full_name |  | ['<Data Name=(\'|")AccountName(\'|")>(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|<]+\.[^\]\s"\\,\|<]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^<]+))<'] |
| edit_regex_field | user |  | ['<Data Name=(\'|")AccountName(\'|")>(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|<]+\.[^\]\s"\\,\|<]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^<]+))<'] |