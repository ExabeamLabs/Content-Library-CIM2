# Code Changes for microsoft-evsecurity-xml-group-member-list-4799-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | src_user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>({src_user}({user}(LOCAL SERVICE|[\w\.\-\!\#\^\~\s]{1,40}\$?)))'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>({src_user}({user}(LOCAL SERVICE|[\w\.\-\!\#\^\~\s]{1,40}\$?)))'] |