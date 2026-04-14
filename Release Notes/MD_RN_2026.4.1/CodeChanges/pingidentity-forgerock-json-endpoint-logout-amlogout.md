# Code Changes for pingidentity-forgerock-json-endpoint-logout-amlogout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'domain', 'email_address', 'group_name', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | user |  | ['exa_json_path=$..principal[0],exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({additional_info}[^"$]+))', 'exa_json_path=$..userId,exa_regex=id=({user}[\w\.\-\!\#\^\~]{1,40}\$?),ou=user,o=({group_name}[^,]+),ou=services,dc=({domain}[^,]+),'] |
| added_regex_field | additional_info |  | ['exa_json_path=$..principal[0],exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({additional_info}[^"$]+))'] |
| added_regex_field | email_address |  | ['exa_json_path=$..principal[0],exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({additional_info}[^"$]+))'] |