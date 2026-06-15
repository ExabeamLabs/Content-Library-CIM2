# Code Changes for postfix-postfix-kv-email-queue (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['\Wto=<({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | dest_email_domain |  | ['\Wto=<({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_address |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| edit_regex_field | email_domain |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| edit_regex_field | src_host |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| edit_regex_field | src_user |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| edit_regex_field | user |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|>]+)))'] |