# Code Changes for imperva-securesphere-cef-database-query-success-securesphere (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'app', 'db_name', 'db_operation', 'db_query', 'db_schema', 'db_user', 'dest_ip', 'dest_port', 'domain', 'host', 'response_size', 'service_name', 'src_host', 'src_ip', 'src_port', 'table_name', 'time', 'user'] |
| edit_regex_field | db_user |  | ['\WdbUsername="(|({domain}[^"\\]+)\\)?(|({account}({db_user}[^"\\]+)))"'] |
| edit_regex_field | domain |  | ['\WdbUsername="(|({domain}[^"\\]+)\\)?(|({account}({db_user}[^"\\]+)))"', '\WsrcHost="(|({domain}[^"\\]+)\\)?(|({src_host}[\w\-.]+))"'] |
| added_regex_field | account |  | ['\WdbUsername="(|({domain}[^"\\]+)\\)?(|({account}({db_user}[^"\\]+)))"'] |
| removed_attribute | DupFields |  | N/A |