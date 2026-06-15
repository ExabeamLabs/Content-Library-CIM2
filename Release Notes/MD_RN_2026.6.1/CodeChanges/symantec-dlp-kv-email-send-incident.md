# Code Changes for symantec-dlp-kv-email-send-incident (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['[\s,]recipients="+\s*(N\/A|({email_recipients}(?:({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))(?:\s*,\s*[^\s"@,]+@[^\s@",]+?\s*?)*)\s*"*,)'] |
| edit_regex_field | dest_email_domain |  | ['[\s,]recipients="+\s*(N\/A|({email_recipients}(?:({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))(?:\s*,\s*[^\s"@,]+@[^\s@",]+?\s*?)*)\s*"*,)'] |
| edit_regex_field | email_address |  | ['[\s,]sender="+\s*({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| edit_regex_field | email_domain |  | ['[\s,]sender="+\s*({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| edit_regex_field | email_recipients |  | ['[\s,]recipients="+\s*(N\/A|({email_recipients}(?:({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))(?:\s*,\s*[^\s"@,]+@[^\s@",]+?\s*?)*)\s*"*,)'] |