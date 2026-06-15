# Code Changes for absolute-siemconnector-json-app-activity-success-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.actorDisplayName,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),exa_match_expr=Contains($.actorObjectType,"User")'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.actorDisplayName,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),exa_match_expr=Contains($.actorObjectType,"User")'] |
| edit_regex_field | user |  | ['exa_json_path=$.actorDisplayName,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),exa_match_expr=Contains($.actorObjectType,"User")'] |