# Code Changes for leef-digitalguardian-dlp-email-alert-out (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['EmailRecipient=(|({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| edit_regex_field | dest_email_domain |  | ['EmailRecipient=(|({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| edit_regex_field | email_address |  | ['EmailSender=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*(\w+=|$)', 'usrName=(?=[^\s]+@[^\s]+)({email_address}[^\s@]+@[^\s]+)'] |
| edit_regex_field | email_domain |  | ['EmailSender=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*(\w+=|$)'] |