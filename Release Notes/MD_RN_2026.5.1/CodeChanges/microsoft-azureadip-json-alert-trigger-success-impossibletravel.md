# Code Changes for microsoft-azureadip-json-alert-trigger-success-impossibletravel (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'email_address', 'full_name', 'location', 'result', 'src_ip', 'src_port', 'tenant_id', 'time', 'user', 'user_upn'] |
| edit_regex_field | email_address |  | ['"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?))"', 'exa_json_path=$.userStates[0].userPrincipalName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?)'] |
| edit_regex_field | user |  | ['"accountName":\s*"(({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', '"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?))"', 'exa_json_path=$.userStates[0].userPrincipalName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?)'] |
| added_regex_field | tenant_id |  | ['"azureTenantId":\s*"({tenant_id}[^"]+)"'] |