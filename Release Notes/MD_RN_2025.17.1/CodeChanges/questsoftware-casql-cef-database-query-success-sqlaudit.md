# Code Changes for questsoftware-casql-cef-database-query-success-sqlaudit (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['\sdomain=({domain}[^\s]+)', '\ssqlSessionLoginName=(({domain}NT AUTHORITY|[^\\\s]+)[\\]+)?({user}SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON|[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| edit_regex_field | user |  | ['\ssqlSessionLoginName=(({domain}NT AUTHORITY|[^\\\s]+)[\\]+)?({user}SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON|[\w\.\-\!\#\^\~]{1,40}\$?)'] |