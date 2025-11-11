# Code Changes for imperva-securesphere-cef-database-logout-success-logout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'alert_id', 'app', 'db_name', 'db_query', 'db_schema', 'db_user', 'dest_ip', 'dest_port', 'domain', 'event_category', 'group_name', 'host', 'object', 'operation', 'policy_name', 'service_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | db_user |  | ['duser=(({domain}[^\\\s]+)\\+)?({account}({db_user}[^\s\|]+))'] |
| edit_regex_field | domain |  | ['duser=(({domain}[^\\\s]+)\\+)?({account}({db_user}[^\s\|]+))'] |
| added_regex_field | account |  | ['duser=(({domain}[^\\\s]+)\\+)?({account}({db_user}[^\s\|]+))'] |
| removed_attribute | DupFields |  | N/A |