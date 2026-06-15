# Code Changes for gamma-g-kv-alert-trigger-success-security-violation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\'email_address\':\s+\'({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\'', "'email_address':\s+'({email_address}[^']+)'"] |
| edit_regex_field | email_domain |  | ['\'email_address\':\s+\'({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\''] |