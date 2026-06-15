# Code Changes for vmware-carbonblackedr-json-app-activity-success-actor (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['exa_json_path=$.actor,exa_regex=(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s"]+?\.corp))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.actor,exa_regex=(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s"]+?\.corp))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.actor,exa_regex=(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s"]+?\.corp))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['exa_json_path=$.actor,exa_regex=(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s"]+?\.corp))|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |