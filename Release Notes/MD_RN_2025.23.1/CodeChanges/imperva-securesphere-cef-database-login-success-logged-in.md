# Code Changes for imperva-securesphere-cef-database-login-success-logged-in (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'db_user', 'dest_host', 'dest_ip', 'domain', 'host', 'severity', 'src_ip', 'time', 'user'] |
| edit_regex_field | domain |  | ['suser=(({domain}[^\\"=]+)\\+)?({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+?='] |
| edit_regex_field | user |  | ['suser=(({domain}[^\\"=]+)\\+)?({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+?='] |
| added_regex_field | db_user |  | ['suser=(({domain}[^\\"=]+)\\+)?({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+?='] |
| removed_attribute | DupFields |  | N/A |