# Code Changes for okta-amfa-json-group-member-add-success-active (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.profile.email,exa_regex=^(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.profile.email,exa_regex=^(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| edit_regex_field | user |  | ['exa_json_path=$.profile.displayName,exa_regex=^((({domain}[^\s\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^\s,]+([\s,]+\s*[^\s"]+)+?))$', 'exa_json_path=$.profile.email,exa_regex=^(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |