# Code Changes for auth0-a-json-endpoint-login-fail-fp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | auth_type |  | ['exa_json_path=$..user_id,exa_regex=((({auth_type}[^|"]+)\|({domain}[^|"]+)\|[^\|]*?)|(({=auth_type}[^|"]+)\|))'] |
| edit_regex_field | domain |  | ['exa_json_path=$..user_id,exa_regex=((({auth_type}[^|"]+)\|({domain}[^|"]+)\|[^\|]*?)|(({=auth_type}[^|"]+)\|))', 'exa_json_path=$..user_name,exa_regex=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,\.]+))?)$'] |
| edit_regex_field | user |  | ['exa_json_path=$..user_name,exa_regex=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,\.]+))?)$', 'exa_regex="user_name":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))'] |