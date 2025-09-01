# Code Changes for microsoft-azuread-xml-user-password-modify-success-10014 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | full_name |  | ['<Data Name\\*=(\'|")Data2(\'|")>({full_name}[^<]+)</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")Data1(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | user_sid |  | ['Security UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")'] |