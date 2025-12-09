# Code Changes for zscaler-pa-json-user-unlock-success-accountunlock (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.User,exa_regex=(({email_address}[^"@]+@({email_domain}[^".]+\.[^"]+))|({user}ZPA System User|[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.User,exa_regex=(({email_address}[^"@]+@({email_domain}[^".]+\.[^"]+))|({user}ZPA System User|[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))'] |
| edit_regex_field | full_name |  | ['exa_json_path=$.User,exa_regex=(({email_address}[^"@]+@({email_domain}[^".]+\.[^"]+))|({user}ZPA System User|[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))'] |
| edit_regex_field | user |  | ['exa_json_path=$.User,exa_regex=(({email_address}[^"@]+@({email_domain}[^".]+\.[^"]+))|({user}ZPA System User|[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))'] |