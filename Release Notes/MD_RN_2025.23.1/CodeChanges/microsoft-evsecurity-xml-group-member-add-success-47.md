# Code Changes for microsoft-evsecurity-xml-group-member-add-success-47 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(\#011)*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\#\d+)*\s*<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(\#011)*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\#\d+)*\s*<', 'Subject:.+?Account Name:\s*(#011)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(#011)*\s*Account Domain'] |
| removed_attribute | DupFields |  | N/A |