# Code Changes for microsoft-m365auditlogs-sk4-app-activity-graphdirectoryauditlogs (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"+userPrincipalName"+:"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}[^"]+))', '"displayName":"({email_address}[^@"]+@[^."]+\.[^"]+)","type":"User"'] |
| edit_regex_field | email_domain |  | ['"+userPrincipalName"+:"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}[^"]+))'] |
| edit_regex_field | user_id |  | ['"+userPrincipalName"+:"+(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user_id}[^"]+))'] |