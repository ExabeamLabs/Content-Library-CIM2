# Code Changes for forcepoint-dlp-cef-email-send-receive-endpointemail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['duser=({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^;\]\s"\\,\|]+))[^=]*)\s+\w+='] |
| edit_regex_field | dest_email_domain |  | ['duser=({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^;\]\s"\\,\|]+))[^=]*)\s+\w+='] |
| edit_regex_field | email_address |  | ['\Wsuser=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['\Wsuser=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_recipients |  | ['duser=({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^;\]\s"\\,\|]+))[^=]*)\s+\w+='] |