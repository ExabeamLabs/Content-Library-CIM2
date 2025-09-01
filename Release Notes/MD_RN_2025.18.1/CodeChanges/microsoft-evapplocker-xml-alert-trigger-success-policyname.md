# Code Changes for microsoft-evapplocker-xml-alert-trigger-success-policyname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")User(\'|")>(({domain}[^\\<]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")User(\'|")>(({domain}[^\\<]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}.+?)(\'|")/>'] |