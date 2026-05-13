# Code Changes for microsoft-evazureadppdca-xml-user-password-reset-fail-10017 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"] |
| edit_regex_field | full_name |  | ['<Data Name\\*=(\'|")Data2(\'|")>({full_name}[^<]+)</Data>', 'FullName:\s+({full_name}[^<]+?)\s+</Message>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")Data1(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>', 'UserName:\s*({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |