# Code Changes for azure-azuremfa-json-user-disable-accountdisabled (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_email_address', 'dest_user', 'src_ip', 'src_port'] |
| edit_regex_field | dest_email_address |  | ['exa_json_path=$.userPrincipalName,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[^@",\s]+))'] |
| removed_regex_field | dest_email_domain |  | [] |
| edit_regex_field | dest_user |  | ['exa_json_path=$.userPrincipalName,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[^@",\s]+))'] |