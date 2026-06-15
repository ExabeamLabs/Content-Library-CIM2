# Code Changes for microsoft-o365-json-app-login-success-loginsuccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"+userPrincipalName"+:"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}[^"]+))'] |
| edit_regex_field | email_domain |  | ['"+userPrincipalName"+:"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}[^"]+))'] |
| edit_regex_field | user_id |  | ['"+userDisplayName"+:"+(({full_name}[^\s"]+\s+[^"]+)|({user_id}[^"]+))', '"+userId"+:"+({user_id}[^"]+)', '"+userPrincipalName"+:"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}[^"]+))'] |