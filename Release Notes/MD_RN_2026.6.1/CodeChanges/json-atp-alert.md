# Code Changes for json-atp-alert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_regex="userStates":\s*[^\]]+?"userPrincipalName":\s*"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}[^"]+))"'] |
| edit_regex_field | full_name |  | ['exa_regex="userStates":\s*[^\]]+?"userPrincipalName":\s*"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}[^"]+))"'] |