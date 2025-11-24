# Code Changes for mcafee-mdam-kv-database-dbactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'app', 'db_domain', 'db_name', 'db_operation', 'db_query', 'db_schema', 'db_user', 'domain', 'host', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | db_domain |  | ['db_user="(NULL|(({db_domain}[^"]+)\\+)?({account}({db_user}.+?))\s*)"'] |
| edit_regex_field | db_user |  | ['db_user="(NULL|(({db_domain}[^"]+)\\+)?({account}({db_user}.+?))\s*)"'] |
| added_regex_field | account |  | ['db_user="(NULL|(({db_domain}[^"]+)\\+)?({account}({db_user}.+?))\s*)"'] |
| removed_attribute | DupFields |  | N/A |