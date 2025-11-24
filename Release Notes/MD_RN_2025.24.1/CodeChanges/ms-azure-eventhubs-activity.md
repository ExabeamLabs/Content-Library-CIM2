# Code Changes for ms-azure-eventhubs-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"+initiatedBy[^}]+"+userPrincipalName\\?"+:\s*\\?"+({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"+', 'exa_regex="+initiatedBy[^}]+"+userPrincipalName\\?"+:\s*\\?"+({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"+'] |
| edit_regex_field | email_domain |  | ['"+initiatedBy[^}]+"+userPrincipalName\\?"+:\s*\\?"+({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"+', 'exa_regex="+initiatedBy[^}]+"+userPrincipalName\\?"+:\s*\\?"+({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\\?"+'] |