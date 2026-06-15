# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-successfullyloggedon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_user |  | ['New Logon(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)[^\}:]*?Account Name(:|=)\s*(\\t|\\r|\\n)*(-|SYSTEM|(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))[\s;]*(\\t|\\r|\\n)*Account Domain(:|=)'] |
| edit_regex_field | user |  | ['New Logon(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)[^\}:]*?Account Name(:|=)\s*(\\t|\\r|\\n)*(-|SYSTEM|(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))[\s;]*(\\t|\\r|\\n)*Account Domain(:|=)'] |
| edit_regex_field | user_upn |  | ['New Logon(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)[^\}:]*?Account Name(:|=)\s*(\\t|\\r|\\n)*(-|SYSTEM|(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))[\s;]*(\\t|\\r|\\n)*Account Domain(:|=)'] |