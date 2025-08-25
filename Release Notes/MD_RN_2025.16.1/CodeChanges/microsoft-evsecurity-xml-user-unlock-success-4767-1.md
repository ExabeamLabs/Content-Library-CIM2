# Code Changes for microsoft-evsecurity-xml-user-unlock-success-4767-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | src_user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>\s*(SYSTEM|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*</Data>'] |