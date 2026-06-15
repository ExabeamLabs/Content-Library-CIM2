# Code Changes for google-workspace-cef-file-permission-modify-success-aclchange (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | [',"parameters":[^=]*?name":"target_user","value":"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^@",\s]+))"[^=]*?"'] |
| edit_regex_field | dest_email_domain |  | [',"parameters":[^=]*?name":"target_user","value":"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^@",\s]+))"[^=]*?"'] |
| edit_regex_field | dest_user |  | [',"parameters":[^=]*?name":"target_user","value":"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^@",\s]+))"[^=]*?"'] |
| edit_regex_field | email_address |  | ['"actor"\s*:\s*\{[^=]*?"email"\s*:\s*"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| edit_regex_field | email_domain |  | ['"actor"\s*:\s*\{[^=]*?"email"\s*:\s*"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |