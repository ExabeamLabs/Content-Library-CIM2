# Code Changes for box-ccm-cef-file-success-move (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['owned_by"+:.+?"login"+:"+({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | dest_email_domain |  | ['owned_by"+:.+?"login"+:"+({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_address |  | ['"login":"({email_address}[^\s",@]+@[^\s",@]+)', 'created_by"+\s*:\s*[^\}]+?[^\w]login"+\s*:\s*"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | email_domain |  | ['created_by"+\s*:\s*[^\}]+?[^\w]login"+\s*:\s*"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['"login":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', 'created_by"+\s*:\s*[^\}]+?[^\w]login"+\s*:\s*"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |