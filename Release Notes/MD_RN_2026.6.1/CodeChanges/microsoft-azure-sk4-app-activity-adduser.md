# Code Changes for microsoft-azure-sk4-app-activity-adduser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['TargetResources":\s*"\[[^|]+userPrincipalName\\":\s*\\"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^"]+?))\\?"'] |
| edit_regex_field | dest_email_domain |  | ['TargetResources":\s*"\[[^|]+userPrincipalName\\":\s*\\"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^"]+?))\\?"'] |
| edit_regex_field | dest_user |  | ['TargetResources":\s*"\[[^|]+userPrincipalName\\":\s*\\"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^"]+?))\\?"'] |