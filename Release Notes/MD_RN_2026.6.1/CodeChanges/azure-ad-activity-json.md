# Code Changes for azure-ad-activity-json (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['exa_json_path=$..targetResources[*].userPrincipalName,exa_regex=(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[^@",\s]+))'] |
| edit_regex_field | dest_user |  | ['exa_json_path=$..targetResources[*].userPrincipalName,exa_regex=(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[^@",\s]+))', 'exa_json_path=$..targetResources[*].userPrincipalName,exa_regex=({dest_user}[^@\"]+)'] |
| edit_regex_field | email_address |  | ['exa_json_path=$..initiatedBy.user.userPrincipalName,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)'] |