# Code Changes for microsoft-evsecurity-xml-file-permission-modify-4670 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | src_user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>({src_user}({user}(LOCAL SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| edit_regex_field | user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>({src_user}({user}(LOCAL SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?)))<', 'Subject:\s*([^"]+?)Account Name:\s*(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |