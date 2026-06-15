# Code Changes for proofpoint-tap-json-email-receive-fail-emailreceived (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['\'envelope\':\s*\{.*\'rcpts\':\s*\[\'({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\\'\|]+)).*?)\'\]'] |
| edit_regex_field | dest_email_domain |  | ['\'envelope\':\s*\{.*\'rcpts\':\s*\[\'({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\\'\|]+)).*?)\'\]'] |
| edit_regex_field | email_address |  | ['\'from\':\s*\[?\'[^@]*?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,\\';\|]+))'] |
| edit_regex_field | email_domain |  | ['\'from\':\s*\[?\'[^@]*?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,\\';\|]+))'] |
| edit_regex_field | email_recipients |  | ['\'envelope\':\s*\{.*\'rcpts\':\s*\[\'({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\\'\|]+)).*?)\'\]'] |