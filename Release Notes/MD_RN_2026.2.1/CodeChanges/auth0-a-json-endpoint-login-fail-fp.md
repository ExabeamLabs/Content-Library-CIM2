# Code Changes for auth0-a-json-endpoint-login-fail-fp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['exa_json_path=$..user_id,exa_regex=((({auth_type}[^|"]+)\|({domain}[^|"]+)\|[^\|]*?)|(({=auth_type}[^|"]+)\|))', 'exa_regex="user_name":"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,\.]+))?)$'] |
| edit_regex_field | user |  | ['exa_regex="user_name":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))', 'exa_regex="user_name":"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,\.]+))?)$'] |