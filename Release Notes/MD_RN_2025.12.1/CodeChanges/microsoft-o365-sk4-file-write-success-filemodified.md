# Code Changes for microsoft-o365-sk4-file-write-success-filemodified (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | email_address | ['"(UserId|userPrincipalName)":"({email_address}[^:@]+@({email_domain}[^"]+\.[^"]+))"'] | ['"(UserId|userPrincipalName)":"({email_address}[^:@]+@({email_domain}[^"]+\.[^"]+))"', 'exa_json_path=$.UserId,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)$'] |