# Code Changes for vectra-cd-json-alert-trigger-success-accountscoring (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['exa_json_path=$.name,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,]+))?))'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.name,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,]+))?))'] |
| edit_regex_field | user |  | ['exa_json_path=$.name,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,]+))?))'] |