# Code Changes for microsoft-evsecurity-xml-user-unlock-success-4767-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | src_user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>\s*(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*</Data>'] |
| edit_regex_field | user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>\s*(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*</Data>', 'Subject:[\s\S]*?Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Account Domain:\s*({domain}.+?)\s*Logon ID:\s*({login_id}.+?)\s*Target Account:'] |
| removed_attribute | DupFields |  | N/A |