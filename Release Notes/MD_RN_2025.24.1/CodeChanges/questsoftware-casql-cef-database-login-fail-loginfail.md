# Code Changes for questsoftware-casql-cef-database-login-fail-loginfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'db_name', 'db_object', 'db_operation', 'db_user', 'dest_host', 'dest_ip', 'domain', 'failure_reason', 'host', 'instance_id', 'src_host', 'src_ip', 'time', 'user'] |
| edit_regex_field | domain |  | ['\sdomain=({domain}[^\s]+)', '\ssqlSessionLoginName=(({domain}NT AUTHORITY|[^\\\s]+)[\\]+)?({db_user}({user}SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON|[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['\ssqlSessionLoginName=(({domain}NT AUTHORITY|[^\\\s]+)[\\]+)?({db_user}({user}SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON|[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | db_user |  | ['\ssqlSessionLoginName=(({domain}NT AUTHORITY|[^\\\s]+)[\\]+)?({db_user}({user}SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON|[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |