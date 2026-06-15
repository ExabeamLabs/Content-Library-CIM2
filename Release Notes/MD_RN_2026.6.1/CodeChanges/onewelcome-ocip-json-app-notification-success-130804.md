# Code Changes for onewelcome-ocip-json-app-notification-success-130804 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['exa_json_path=$.account,exa_regex=(-|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?)'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.account,exa_regex=(-|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?)'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.account,exa_regex=(-|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?)'] |
| edit_regex_field | user |  | ['exa_json_path=$.account,exa_regex=(-|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?)'] |