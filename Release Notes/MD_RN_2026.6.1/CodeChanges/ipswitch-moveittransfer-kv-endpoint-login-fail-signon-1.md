# Code Changes for ipswitch-moveittransfer-kv-endpoint-login-fail-signon-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['User\s\'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^\']+))?\'\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\)'] |
| edit_regex_field | email_domain |  | ['User\s\'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^\']+))?\'\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\)'] |
| edit_regex_field | full_name |  | ['User\s\'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^\']+))?\'\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\)'] |
| edit_regex_field | user |  | ['User\s\'(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^\']+))?\'\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\)', '\sUsername:\s*(Automation|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |