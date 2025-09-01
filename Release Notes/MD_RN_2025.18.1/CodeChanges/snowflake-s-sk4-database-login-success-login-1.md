# Code Changes for snowflake-s-sk4-database-login-success-login-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'db_user', 'failure_reason', 'query_id', 'result', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | time |  | ['"EVENT_TIMESTAMP":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '"EVENT_TIMESTAMP":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)'] |
| edit_regex_field | user |  | ['"USER_NAME":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', '\ssuser=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | failure_reason |  | ['"ERROR_MESSAGE":"({failure_reason}[^"]+)'] |