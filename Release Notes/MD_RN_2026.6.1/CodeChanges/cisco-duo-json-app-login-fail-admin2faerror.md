# Code Changes for cisco-duo-json-app-login-fail-admin2faerror (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_regex="email\\"+:\s*\\"+({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\"+'] |
| edit_regex_field | email_domain |  | ['exa_regex="email\\"+:\s*\\"+({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\"+'] |