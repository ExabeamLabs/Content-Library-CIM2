# Code Changes for microsoft-azuread-json-group-member-remove-success-groupmemberremoved (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['targetResources":[^\}]+userPrincipalName":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(,|")'] |
| edit_regex_field | email_domain |  | ['targetResources":[^\}]+userPrincipalName":"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(,|")'] |