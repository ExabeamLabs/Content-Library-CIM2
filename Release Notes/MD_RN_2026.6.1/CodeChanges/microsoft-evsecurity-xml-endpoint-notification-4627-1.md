# Code Changes for microsoft-evsecurity-xml-endpoint-notification-4627-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>(({dest_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| edit_regex_field | dest_user |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>(({dest_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| edit_regex_field | email_address |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>(({dest_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>(({dest_email_address}({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |