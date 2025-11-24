# Code Changes for apache-cassandradb-kv-database-login-success-auth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'db_user', 'dest_ip', 'dest_port', 'event_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | db_user |  | ['\|authenticated:({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | user |  | ['\|authenticated:({db_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |