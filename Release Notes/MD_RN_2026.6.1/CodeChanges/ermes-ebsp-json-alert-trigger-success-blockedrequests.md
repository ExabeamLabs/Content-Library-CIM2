# Code Changes for ermes-ebsp-json-alert-trigger-success-blockedrequests (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['exa_json_path=$.username,exa_regex=^(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(?<!local)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?))$'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.username,exa_regex=^(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(?<!local)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?))$'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.username,exa_regex=^(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(?<!local)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?))$'] |
| edit_regex_field | user |  | ['exa_json_path=$.username,exa_regex=^(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(?<!local)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?))$'] |