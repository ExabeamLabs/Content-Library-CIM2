# Code Changes for microsoft-evsecurity-json-endpoint-login-fail-4625-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_user |  | ['"TargetUserName\\?":\\?"\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['"TargetUserName\\?":\\?"\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | user_upn |  | ['"TargetUserName\\?":\\?"\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |