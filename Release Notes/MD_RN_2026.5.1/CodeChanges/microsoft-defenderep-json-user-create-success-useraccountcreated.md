# Code Changes for microsoft-defenderep-json-user-create-success-useraccountcreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$..AccountUpn,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),exa_match_expr=!Contains(tolower($..AccountUpn), "null")'] |
| edit_regex_field | user |  | ['exa_json_path=$..AccountUpn,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),exa_match_expr=!Contains(tolower($..AccountUpn), "null")'] |