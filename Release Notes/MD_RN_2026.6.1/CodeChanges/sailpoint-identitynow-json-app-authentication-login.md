# Code Changes for sailpoint-identitynow-json-app-authentication-login (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.actor.name,exa_regex=((?i)Not Available|unknown|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|(({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | full_name |  | ['exa_json_path=$.actor.name,exa_regex=((?i)Not Available|unknown|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|(({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['exa_json_path=$.actor.name,exa_regex=((?i)Not Available|unknown|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|(({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |