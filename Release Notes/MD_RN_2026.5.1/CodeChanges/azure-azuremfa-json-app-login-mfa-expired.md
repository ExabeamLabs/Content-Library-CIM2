# Code Changes for azure-azuremfa-json-app-login-mfa-expired (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['email_address', 'src_ip', 'src_port', 'user'] |
| removed_regex_field | dest_email_address |  | [] |
| removed_regex_field | dest_user |  | [] |
| added_regex_field | email_address |  | ['exa_json_path=$..userPrincipalName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?)'] |
| added_regex_field | user |  | ['exa_json_path=$..userPrincipalName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?)'] |