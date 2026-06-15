# Code Changes for darktrace-darktrace-cef-alert-trigger-success-darktrace (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"recipients":\["({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)[^\]]*)"\]'] |
| edit_regex_field | email_address |  | ['"from":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)', 'dvchost=[^\s]+?\s({email_address}[^\s@]+\@({email_domain}[^\s]+))?'] |
| edit_regex_field | email_recipients |  | ['"recipients":\["({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)[^\]]*)"\]'] |