# Code Changes for microsoft-evsecurity-kv-user-switch-success-4648-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['Subject(:|=).+?Account Name(:|=)\s*(\\t|\\r|\\n)*(?:-|SYSTEM|(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))[\s;]*(\\t|\\r|\\n)*Account Domain(:|=)'] |
| edit_regex_field | user_upn |  | ['Subject(:|=).+?Account Name(:|=)\s*(\\t|\\r|\\n)*(?:-|SYSTEM|(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))[\s;]*(\\t|\\r|\\n)*Account Domain(:|=)'] |