# Code Changes for microsoft-o365-sk4-email-receive-success-inbound (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"RecipientAddress":"({dest_email_address}({email_recipients}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"'] |
| edit_regex_field | email_address |  | ['"SenderAddress":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| edit_regex_field | email_domain |  | ['"SenderAddress":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| edit_regex_field | email_recipients |  | ['"RecipientAddress":"({dest_email_address}({email_recipients}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"'] |