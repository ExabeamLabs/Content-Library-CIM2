# Code Changes for ibm-guardium-kv-database-query-success-dbuser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'app_protocol', 'db_name', 'db_operation', 'db_user', 'host', 'rule_description', 'server_group', 'service_name', 'src_host', 'src_interface', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | db_user |  | ['\WDBUser="?({account}({db_user}[^;\|"]+?))\s*(?:;|"|\||$)'] |
| added_regex_field | account |  | ['\WDBUser="?({account}({db_user}[^;\|"]+?))\s*(?:;|"|\||$)'] |
| removed_attribute | DupFields |  | N/A |