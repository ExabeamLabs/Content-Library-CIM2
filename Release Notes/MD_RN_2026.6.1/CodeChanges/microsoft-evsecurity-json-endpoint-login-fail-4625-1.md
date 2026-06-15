# Code Changes for microsoft-evsecurity-json-endpoint-login-fail-4625-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_user |  | ['exa_json_path=$..TargetUserName,exa_regex=^(-|(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))$'] |
| edit_regex_field | user |  | ['exa_json_path=$..TargetUserName,exa_regex=^(-|(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))$'] |
| edit_regex_field | user_upn |  | ['exa_json_path=$..TargetUserName,exa_regex=^(-|(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))$'] |