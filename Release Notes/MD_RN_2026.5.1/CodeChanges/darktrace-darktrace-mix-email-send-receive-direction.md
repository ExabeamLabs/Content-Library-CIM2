# Code Changes for darktrace-darktrace-mix-email-send-receive-direction (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"recipients":\["({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))[^\]]*?)"\]'] |
| edit_regex_field | dest_email_domain |  | ['"recipients":\["({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))[^\]]*?)"\]'] |
| edit_regex_field | email_address |  | ['"from":"(|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))"'] |
| edit_regex_field | email_domain |  | ['"from":"(|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))"'] |
| edit_regex_field | email_recipients |  | ['"recipients":\["({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))[^\]]*?)"\]'] |