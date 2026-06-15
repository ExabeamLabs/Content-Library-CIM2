# Code Changes for bitglass-casb-mix-app-login-fail-loginfailure (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"email":\s*"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"', 'exa_json_path=$.email,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['"email":\s*"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"', 'exa_json_path=$.email,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |