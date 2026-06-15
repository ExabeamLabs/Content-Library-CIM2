# Code Changes for proofpoint-tappod-sk4-email-receive-fail-emailreceived (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"rcpts"+:\s*\["+({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?)"*\]'] |
| edit_regex_field | dest_email_domain |  | ['"rcpts"+:\s*\["+({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?)"*\]'] |
| edit_regex_field | email_address |  | ['"from"+:\s*\[?"+?({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['"from"+:\s*\[?"+?({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_recipients |  | ['"rcpts"+:\s*\["+({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*?)"*\]'] |
| edit_regex_field | full_name |  | ['"from"+:\s*\[?"+?({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |