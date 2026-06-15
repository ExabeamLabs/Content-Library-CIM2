# Code Changes for juniper-ps-str-vpn-login-success-fullycompliant (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account |  | [' for user \[\'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\'\]'] |
| edit_regex_field | email_address |  | [' for user \[\'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\'\]'] |
| edit_regex_field | email_domain |  | [' for user \[\'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\'\]'] |
| edit_regex_field | user |  | [' for user \[\'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\'\]'] |