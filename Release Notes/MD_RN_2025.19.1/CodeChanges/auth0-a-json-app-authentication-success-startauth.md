# Code Changes for auth0-a-json-app-authentication-success-startauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['exa_json_path=$..user_id,exa_regex=((({auth_type}[^|"]+)\|({domain}[^|"]+)\|([\w\.\-]{1,40}\$?))|(({=auth_type}[^|"]+)\|))', 'exa_json_path=$..user_name,exa_regex=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?|)', 'user_id"+:"+((({auth_type}[^|"]+)\|({domain}[^|"]+)\|([\w\.\-]{1,40}\$?))|(({=auth_type}[^|"]+)\|))'] |
| edit_regex_field | user |  | ['exa_json_path=$..user_name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))', 'exa_json_path=$..user_name,exa_regex=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?|)', 'user_name"+:"+(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))"'] |