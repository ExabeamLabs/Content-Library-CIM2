# Code Changes for microsoft-azuread-sk4-user-password-modify-success-userpasswordchange (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['TargetResources":"\[\{[^\]]+?userPrincipalName\\?":\\?"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^"]+?))\\?"'] |
| edit_regex_field | dest_email_domain |  | ['TargetResources":"\[\{[^\]]+?userPrincipalName\\?":\\?"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^"]+?))\\?"'] |
| edit_regex_field | dest_user |  | ['TargetResources":"\[\{[^\]]+?displayName\\?":\\?"?(null|({dest_user}[^"]+?))\\?"?', 'TargetResources":"\[\{[^\]]+?userPrincipalName\\?":\\?"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^"]+?))\\?"'] |