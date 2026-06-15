# Code Changes for zscaler-ia-str-app-activity-apirequest (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"user_email":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', '\suser=(?=[^\s]+@[^\s]+)({email_address}[^\s@]+@[^\s@]+)\s*(\w+=|$)', 'login=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['"user_email":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |