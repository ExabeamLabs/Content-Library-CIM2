# Code Changes for oracle-db-xml-database-login-success-dbauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'db_name', 'db_user', 'process_id', 'protocol', 'result', 'session_id', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | db_user |  | ['<DB_User>(\/|({account}({db_user}.+?)))</DB_User>'] |
| added_regex_field | account |  | ['<DB_User>(\/|({account}({db_user}.+?)))</DB_User>'] |
| removed_attribute | DupFields |  | N/A |