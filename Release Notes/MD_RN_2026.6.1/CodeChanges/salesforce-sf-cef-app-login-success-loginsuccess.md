# Code Changes for salesforce-sf-cef-app-login-success-loginsuccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['suser=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['suser=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |