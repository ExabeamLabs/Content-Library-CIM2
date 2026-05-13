# Code Changes for microsoft-evazureadppdca-xml-app-notification-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | full_name |  | ['(30022|30021).*?<Data Name\\*=(\'|")Data2(\'|")>({full_name}[^<]+)<\/Data>', 'FullName:\s+({full_name}[^<]+?)\s+</Message>'] |
| edit_regex_field | user |  | ['(30022|30021).*?<Data Name\\*=(\'|")Data1(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>', 'UserName:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |