# Code Changes for crowdstrike-falcon-json-app-login-streamstarted-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.attributes.usr.id,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({user_id}api-client-id:[^"]+))$'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.attributes.usr.id,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({user_id}api-client-id:[^"]+))$'] |
| edit_regex_field | user |  | ['exa_json_path=$.attributes.usr.id,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({user_id}api-client-id:[^"]+))$'] |
| edit_regex_field | user_id |  | ['exa_json_path=$.attributes.usr.id,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({user_id}api-client-id:[^"]+))$'] |