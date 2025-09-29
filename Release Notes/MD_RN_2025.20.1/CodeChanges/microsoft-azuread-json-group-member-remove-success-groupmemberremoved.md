# Code Changes for microsoft-azuread-json-group-member-remove-success-groupmemberremoved (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account_id |  | ['targetResources":[^\}]+"id":"({account_id}[^",]+)'] |
| edit_regex_field | app |  | ['"app":\{[^\}]+displayName":"({app}[^",]+)', 'loggedByService":"({app}[^",]+)'] |
| edit_regex_field | email_address |  | ['targetResources":[^\}]+userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(,|")'] |
| edit_regex_field | email_domain |  | ['targetResources":[^\}]+userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(,|")'] |
| edit_regex_field | group_name |  | ['targetResources":[^\]]+Group\.DisplayName[^\}]+newValue":"\\*"({group_name}[^\\"]+)'] |
| edit_regex_field | user_uid |  | ['targetResources":[^\}]+"id":"({user_uid}[^",]+)'] |