# Code Changes for juniper-ps-str-vpn-login-success-fullycompliant (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'email_address', 'email_domain', 'host', 'result', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | email_address |  | [' for user \[\'(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\'\]'] |
| edit_regex_field | email_domain |  | [' for user \[\'(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\'\]'] |
| edit_regex_field | user |  | [' for user \[\'(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\'\]'] |
| added_regex_field | account |  | [' for user \[\'(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\'\]'] |
| removed_attribute | DupFields |  | N/A |