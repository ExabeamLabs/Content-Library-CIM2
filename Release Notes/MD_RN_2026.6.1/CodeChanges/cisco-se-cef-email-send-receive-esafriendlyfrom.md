# Code Changes for cisco-se-cef-email-send-receive-esafriendlyfrom (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['ESAReplyTo=({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\s]*)\s+(\w+=|$)'] |
| edit_regex_field | dest_email_domain |  | ['ESAReplyTo=({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\s]*)\s+(\w+=|$)'] |
| edit_regex_field | domain |  | ['ESAFriendlyFrom=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s]+))'] |
| edit_regex_field | email_address |  | ['ESAFriendlyFrom=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s]+))'] |
| edit_regex_field | email_domain |  | ['ESAFriendlyFrom=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s]+))'] |
| edit_regex_field | email_recipients |  | ['ESAReplyTo=({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\s]*)\s+(\w+=|$)'] |
| edit_regex_field | user |  | ['ESAFriendlyFrom=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s]+))'] |