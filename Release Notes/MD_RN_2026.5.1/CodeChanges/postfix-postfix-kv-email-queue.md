# Code Changes for postfix-postfix-kv-email-queue (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ssZ"] |
| edit_regex_field | email_address |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| edit_regex_field | email_domain |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| edit_regex_field | src_host |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| edit_regex_field | src_user |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| edit_regex_field | user |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| edit_attribute | activity_type |  | ['email-send:success'] |
| edit_attribute | legacy_activity_type |  | ['dlp-email-alert-out'] |