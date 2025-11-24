# Code Changes for postgresql-p-csv-database-login-success-authentication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'db_name', 'db_user', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | db_user |  | ['\s*user=({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s'] |
| added_regex_field | user |  | ['\s*user=({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s'] |
| removed_attribute | DupFields |  | N/A |