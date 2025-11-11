# Code Changes for auth0-a-json-endpoint-login-fail-fp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_type', 'domain', 'email_address', 'email_domain', 'operation_type', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | user |  | ['exa_json_path=$..user_id,exa_regex=((({auth_type}[^|"]+)\|({domain}[^|"]+)\|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|(({=auth_type}[^|"]+)\|))', 'exa_json_path=$..user_name,exa_regex=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,]+))?)', 'exa_regex="user_name":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))'] |
| added_regex_field | email_address |  | ['exa_regex="user_name":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))'] |
| added_regex_field | email_domain |  | ['exa_regex="user_name":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))'] |