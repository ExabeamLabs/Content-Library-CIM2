# Code Changes for microsoft-mssql-str-database-login-success-18453 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['db_user', 'domain', 'event_code', 'event_name', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | domain |  | ["user '(N\/A|(({domain}[^\\']+)\\+)?({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'"] |
| edit_regex_field | user |  | ["user '(N\/A|(({domain}[^\\']+)\\+)?({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'"] |
| added_regex_field | db_user |  | ["user '(N\/A|(({domain}[^\\']+)\\+)?({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'"] |
| removed_attribute | DupFields |  | N/A |