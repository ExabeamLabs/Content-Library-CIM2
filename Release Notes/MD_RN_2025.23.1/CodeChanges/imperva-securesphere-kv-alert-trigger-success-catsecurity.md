# Code Changes for imperva-securesphere-kv-alert-trigger-success-catsecurity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'category', 'db_name', 'db_query', 'db_schema', 'db_user', 'dest_ip', 'dest_port', 'object', 'operation', 'policy_name', 'server_group', 'service_name', 'sql_error', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | db_user |  | ['db_username="?({account}({db_user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | operation |  | ['operation="({alert_name}({operation}[^"]+))', 'operation=({alert_name}({operation}[^",]+))'] |
| added_regex_field | account |  | ['db_username="?({account}({db_user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | alert_name |  | ['operation="({alert_name}({operation}[^"]+))', 'operation=({alert_name}({operation}[^",]+))'] |
| removed_attribute | DupFields |  | N/A |