# Code Changes for microsoft-o365-sk4-email-send-fail-outbound (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"SenderAddress":"({email_address}({email_user}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+)@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| edit_regex_field | email_domain |  | ['"SenderAddress":"({email_address}({email_user}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+)@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| edit_regex_field | email_user |  | ['"SenderAddress":"({email_address}({email_user}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+)@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |