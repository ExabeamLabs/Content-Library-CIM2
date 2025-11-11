# Code Changes for imperva-securesphere-kv-database-query-success-eventcatquery (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'alert_id', 'app', 'db_query', 'db_user', 'dest_ip', 'dest_port', 'event_category', 'group_name', 'object', 'operation', 'policy_name', 'service_name', 'src_ip', 'src_port', 'src_user', 'time'] |
| edit_regex_field | db_user |  | ['db_username="?({account}({db_user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | account |  | ['db_username="?({account}({db_user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |