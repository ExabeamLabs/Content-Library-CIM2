# Code Changes for postfix-postfix-kv-email-queue (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'host', 'message_id', 'num_recipients', 'src_host', 'src_user', 'time', 'user'] |
| edit_regex_field | email_address |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| edit_regex_field | email_domain |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| edit_regex_field | src_host |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| edit_regex_field | src_user |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| added_regex_field | user |  | ['\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+)))'] |
| removed_attribute | DupFields |  | N/A |