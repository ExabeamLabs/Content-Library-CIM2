# Code Changes for proofpoint-tap-json-email-envelope (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['exa_regex="rcpts"+:\s*\[({email_recipients}"+({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)).*?)\]'] |
| edit_regex_field | dest_email_domain |  | ['exa_regex="rcpts"+:\s*\[({email_recipients}"+({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)).*?)\]'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.envelope.from,exa_regex=({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.envelope.from,exa_regex=({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_recipients |  | ['exa_regex="rcpts"+:\s*\[({email_recipients}"+({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)).*?)\]'] |
| edit_regex_field | full_name |  | ['exa_json_path=$.envelope.from,exa_regex=({full_name}[^"@\s,<>]+\s+[^"@,<>]+?)?\s*\<?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |