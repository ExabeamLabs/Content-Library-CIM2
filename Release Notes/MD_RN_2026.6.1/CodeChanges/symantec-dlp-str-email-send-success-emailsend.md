# Code Changes for symantec-dlp-str-email-send-success-emailsend (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['sender="*(?=[\w.]+@[\w.])({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))("|,|\s*$)'] |
| edit_regex_field | email_domain |  | ['sender="*(?=[\w.]+@[\w.])({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))("|,|\s*$)'] |