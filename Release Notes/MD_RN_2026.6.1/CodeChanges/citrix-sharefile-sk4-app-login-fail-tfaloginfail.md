# Code Changes for citrix-sharefile-sk4-app-login-fail-tfaloginfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"Email":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"', '"UserMakingChangeEmailAddress":"({email_address}[^@"]+@({email_domain}[^@\."]+\.[^"]+))"'] |
| edit_regex_field | email_domain |  | ['"Email":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"', '"UserMakingChangeEmailAddress":"({email_address}[^@"]+@({email_domain}[^@\."]+\.[^"]+))"'] |